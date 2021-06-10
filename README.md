# MySQL
> MySQL CRUD
> 

### 데이터 베이스 생성하기
```SQL
CREATE DATABASE BBS;
```

### 생성한 데이터 베이스로 이동
```SQL
USE BBS;
```

### user 테이블 만들기
```SQL
CREATE TABLE IF NOT EXISTS user (
  userID VARCHAR(20),
  userPassword VARCHAR(20),
  userName VARCHAR(20),
  userGender VARCHAR(20),
  userEmail VARCHAR(20),
  PRIMARY KEY (userID)
);
```

### 생성한 테이블 리스트
```SQL
SHOW TABLES; 
```

### 테이블 칼럼 확인
```SQL
DESC user;
```

### CRUDClass 테이블에 데이타 추가
```SQL
INSERT INTO user VALUES('gildong','12345', '남자', 'name1@email.com');
INSERT INTO user VALUES('sum','111', '여자', 'hohoho1@email.com');
INSERT INTO user VALUES('dengdeng','222', '남자', 'gugu1@email.com');

commit;
```

### 등록된 데이터 리스트 보기
```SQL
SELECT * FROM user;
```

### bbs 테이블 만들기
```SQL
CREATE TABLE IF NOT EXISTS bbs (
  bbsID INT,
  bbsTitle VARCHAR(50),
  userID VARCHAR(20),
  bbsDate DATETIME,
  bbsContent VARCHAR(2048),
  PRIMARY KEY (bbsID)
);
```

### bbs 테이블 내용 수정
```SQL
UPDATE bbs SET bbsTitle = '제목수정', bbsContent = '내용수정' WHERE bbsID = 1;
```

### bbs 테이블 삭제 (행)
```SQL
DELETE FROM CRUDClass WHERE id = 1;
```





