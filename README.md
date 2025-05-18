# nothing

-- 시퀀스 생성
CREATE SEQUENCE posts_seq START WITH 1 INCREMENT BY 1;

-- 테이블 생성
CREATE TABLE posts (
    id NUMBER PRIMARY KEY,
    image_url VARCHAR2(500) NOT NULL,
    caption CLOB,
    created_at TIMESTAMP DEFAULT SYSTIMESTAMP,
    expires_at TIMESTAMP
);

-- 트리거 생성
CREATE OR REPLACE TRIGGER trg_posts_id
BEFORE INSERT ON posts
FOR EACH ROW
WHEN (NEW.id IS NULL)
BEGIN
    SELECT posts_seq.NEXTVAL INTO :NEW.id FROM dual;
END;
/
