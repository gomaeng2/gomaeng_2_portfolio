<html>
<head>
    <meta charset="utf-8">
    <title>Simplest jQuery Dropdown Nav Demo</title>
    <link rel="stylesheet" href="http://netdna.bootstrapcdn.com/font-awesome/4.6.2/css/font-awesome.min.css">
    <style>
        @import url(https://fonts.googleapis.com/css?family=Roboto:400,700,500);
        /* main Styles */
        html { box-sizing: border-box; }
        *, *:before, *:after { box-sizing: inherit; }
        body {
            background: #fafafa;
            font-family: "Roboto", sans-serif;
            font-size: 14px;
            margin: 0;
        }
        a { text-decoration: none; }
        .container {
            width: 1000px;
            margin: auto;
        }
        h1 { text-align:center; margin-top:150px;}
        /* Navigation Styles */
        nav { background: #E79CAA; }
        nav ul {
            font-size: 0;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        nav ul li {
            display: inline-block;
            position: relative;
        }
        nav ul li a {
            color: #fff;
            display: block;
            font-size: 14px;
            padding: 15px 35px;
            transition: 0.3s linear;
        }
        nav ul li:hover { background: #d4788f; }
        nav ul li ul {
            border-bottom: 8px solid #d4788f; /*이게 드롭칸 아래 막대기*/
            display: none;
            position: absolute;
            width: 100%;
            left: 0;
        }
        nav ul li ul li {
            border-top: 1px solid #ffdbe1;
            display: block;
        }
        nav ul li ul li:first-child { border-top: none; }
        nav ul li ul li a {
            background: #b1425e;
            display: block;
            padding: 10px 14px;
        }
        nav ul li ul li a:hover { background: #570a18; } /*드롭칸 포인터 올리면 변하는 색상*/
        nav .fa.fa-angle-down { margin-left: 6px; }
        .email {            
            color: #fff; /* 흰색 텍스트 */
            font-size: 14px; /* 폰트 크기를 작게 조정 */       
            display: inline-block; /* 인라인 블록으로 설정 */
            padding-left: 40px; /* 왼쪽 여백 */
            background-color: #E79CAA;
        }
        .email:hover {
            background-color: #E79CAA; /* 배경색을 유지 */
        }
        }
    </style>
</head>

<body>
<nav>
    <div class="container">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Portfolio</a></li>
            <li> <a href="#">Commission<i class='fa fa-angle-down'></i></a>
                <ul>
                    <li><a href="https://www.artmug.kr/index.php?channel=view&uid=41850"target="_blank">【아트머그】 버추얼</a></li>
                    <li><a href="https://www.artmug.kr/index.php?channel=view&uid=42735"target="_blank">【아트머그】 커서 모델</a></li>
                    <li><a href="#">Yet</a></li>
                </ul>
            </li>
            <li class='sub-menu'> <a href="#">SNS<i class='fa fa-angle-down'></i></a>
                <ul>
                    <li><a href="https://x.com/gomaeng_2"target="_blank">X</a></li>
                    <li><a href="https://bsky.app/profile/gomaeng2.bsky.social"target="_blank">Bluesky</a></li>
                    <li><a href="https://www.tiktok.com/@gomaeng_2?is_from_webapp=1&sender_device=pc"target="_blank">틱톡</a></li>
                    <li><a href="https://youtube.com/@gomaeng_2?si=NJoetVUV3V9GF7YY"target="_blank">유튜브</a></li>
                </ul>
            </li>
            <li class='sub-menu'> <a href="#">Question<i class='fa fa-angle-down'></i></a>
                <ul>
                    <li><a href="https://pushoong.com/ask/4732474820"target="_blank">푸슝 ASK</a></li>
                </ul>
            <li><a href="#">Mail</a></li>
            <li><span class="email">✉️: gomaeng_2@naver.com</span></li> <!-- 이메일 주소 추가 -->
        </ul>
    </div>
</nav>

<script src="http://code.jquery.com/jquery-1.12.4.min.js"></script>
<script>
    // 드롭다운 메뉴 기능
    $('nav li').hover(
        function() {
            $('ul', this).stop().slideDown(200);
        },
        function() {
            $('ul', this).stop().slideUp(200);
        }
    );
</script>
</body>
</html>
