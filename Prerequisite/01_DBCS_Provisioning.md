Oracle Cloud에 접속
===================

Subscribe한 서비스 정보를 확인하고 제공된 My Services URL에 접속한다.

![](media/25b2749181cfb01a3a4bdbe54467960c.png)

이메일의 Username과 *임시 패스워드*로 로그인한다.

![](media/b2e7d89631ad5f1b6bea797e4df4ca98.png)

처음 접속 시 임시 패스워드를 변경한다.

![](media/295a71bba3fbf4280abcaebf47fa5af3.png)

접속 후 My Service Dashboard에 들어가게 된다.

![](media/035b8e2ef3b1ab73332281a995361987.png)

아래 Dashboard에는 Java Cloud Service와 Database Cloud Service가 보이지 않으므로
“Customize Dashboard” 메뉴를 선택하여 “Database”와 “Java”를 Dashboard에
추가한다.

![](media/9b0943ea5048135bccaa70763394884b.png)

Dashboard가 다음과 같이 보이게 한다.

![](media/33e464a56cd468ae123dd52b2bdabbdb.png)

스토리지 복제 정책 설정
=======================

스토리지 복제 정책을 설정하기 위해 스토리지 링크를 클릭한다.

![](media/6a19135ebb46b2eeaeeb7d04456817ed.png)

상단의 “서비스 콘솔 열기” 링크를 클릭한다.

![](media/67ba27dd0e91104ae61475efb5d52923.png)

복제 정책을 설정하는 화면이 나오는데, 여기서는 default로 되어 있는
uscom-central-1을 선택하고 Set Policy를 클릭한다.

![](media/7eae5022bb178a9445c911656008ebf1.png)

DBCS 프로비저닝
===============

Database Provisioning을 위해 Database Service Console에 들어간다

![](media/adfd1973c8a1a3f4cb8a8b99537ee21d.png)

처음 접속 화면에서 “Go To Console”을 클릭한다

![](media/4238f11b7a6b98ba2368b384a89046ca.png)

“Create Service” 버튼 클릭

![](media/7a42c1418cf8678ea74e0ac9c26d71a8.png)

서비스 명을 다음과 같은 이름으로 입력한다 (같은 이름으로 생성한다. 다른 이름으로
생성시 Lab이 정상동작 하지 않을 수 있음)

![](media/d11af94713bb814d82952d6e89587bfc.png)

DB이름(SID)는 AlphaDB로 한다.

![](media/46f0c33d1bd4007ed3092ce4f0bf5885.png)

Usable Database Storage(GB)를 **15**로 설정한다.

관리 비밀번호를 “**Welcome1\#**”로 입력한다(다른 패스워드로 입력 시 lab에서
제공하는 script에서 수동으로 패스워드를 수정하는 작업을 해줘야 한다.)

SSH 공용키를 생성하기 위해 편집 버튼을 누른다. Public Key를 새로 만드는 것으로
선택한다.

![](media/0c5cc8fc13572bc799a3af86d20f805c.png)

Key를 다운 받아 둔다

![](media/773b57b8a1a9be32aee2905d26bddb51.png)

아래 설정한 옵션대로 선택하고

Cloud Storage Container는 다음 규칙에 맞게 입력한다.

Storage-**identitydomain**/DBContainer

-   **identitydomain** 부분만 각자에게 할당된 identity domain으로 변경하면 된다

-   identity domain이 kroracle이라면 Storage-kroracle/DBContainer 라고 입력하면
    된다

Cloud Storage User Name은 Dashboard에 로그인한 Username과 Password를 사용하면
된다.

다음 항목은 default로 두고 “Next”를 클릭한다.

![](media/4209b7790c17a3674a6f7ee0ac7ff79d.png)

Confirm 화면에서 정보가 잘 입력되었는지 확인 후 “Create”를 클릭한다.

![](media/1e5114cf0aa788ae91328ad1ca88675e.png)

DB가 프로비저닝 되는지 확인한다.

![](media/1944b4c74dd55ad0bdc106b2f1715c2d.png)

프로비저닝 상세는 Activity 메뉴에서 확인할 수 있다.

![](media/553ba81e84781a8f000d3aa2d44cf6cf.png)

완료가 되면 상태가 Succeeded가 된다. 이 과정이 약 30분 정도 소요된다.

![](media/8224dfa420312ca2b71289700a708e75.png)
