# Scool-blaykor
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>منصة ثانوية أبي بكر بالقايد</title>

<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">

<script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Cairo',sans-serif;
}

body{
background:#031c15;
color:white;
min-height:100vh;
overflow-x:hidden;
}

/* خلفية النجوم */

#particles-js{
position:fixed;
width:100%;
height:100%;
z-index:-1;
}

/* النافبار */

.navbar{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 60px;
background:rgba(255,255,255,0.06);
backdrop-filter:blur(15px);
border-bottom:1px solid rgba(255,255,255,0.1);
}

.logo{
font-size:24px;
font-weight:bold;
color:#ffd700;
transition:0.3s;
}

.logo:hover{
transform:scale(1.1);
}

.navbar a{
color:white;
text-decoration:none;
margin-left:20px;
transition:0.3s;
}

.navbar a:hover{
color:#ffd700;
transform:translateY(-3px);
}

/* الصفحات */

.page{
display:none;
padding:40px;
}

.active{
display:block;
}

/* الصفحة الرئيسية */

.home{
text-align:center;
margin-top:120px;
}

.home h1{
font-size:50px;
margin-bottom:20px;
}

.home p{
font-size:18px;
}

/* الأزرار */

.btn{
padding:14px 35px;
border:none;
border-radius:30px;
background:linear-gradient(135deg,#ffd700,#f5e39a);
font-weight:bold;
cursor:pointer;
margin-top:30px;
transition:0.4s;
}

.btn:hover{
transform:scale(1.1) rotate(-1deg);
}

/* تسجيل الدخول */

.login-box{
width:400px;
margin:auto;
margin-top:80px;
padding:40px;
background:rgba(255,255,255,0.07);
border-radius:20px;
backdrop-filter:blur(20px);
box-shadow:0 10px 40px rgba(0,0,0,0.6);
}

input,select,textarea{
width:100%;
padding:12px;
margin-top:10px;
border-radius:10px;
border:none;
}

/* البطاقات */

.card{
background:rgba(255,255,255,0.08);
padding:25px;
margin-top:25px;
border-radius:20px;
backdrop-filter:blur(20px);
transition:0.4s;
}

.card:hover{
transform:translateY(-8px) scale(1.03);
}

/* زر الانستغرام */

.insta{
display:inline-block;
margin-top:20px;
padding:12px 25px;
background:linear-gradient(45deg,#ff416c,#ff4b2b);
border-radius:25px;
color:white;
text-decoration:none;
transition:0.3s;
}

.insta:hover{
transform:scale(1.1);
}

/* الفوتر */

.footer{
text-align:center;
margin-top:80px;
padding:25px;
border-top:1px solid rgba(255,255,255,0.1);
font-size:14px;
}

</style>

<script>

function showPage(id){
document.querySelectorAll(".page").forEach(p=>p.classList.remove("active"));
document.getElementById(id).classList.add("active");
}

function login(){
let pass=document.getElementById("password").value
let type=document.getElementById("type").value

if(type==="admin"){

if(pass==="JN72R8N8117"){
showPage("admin")
}else{
alert("كلمة السر خاطئة")
}

}else{
showPage("student")
}
}

</script>

</head>

<body>

<div id="particles-js"></div>

<div class="navbar">
<div class="logo">ثانوية أبي بكر بالقايد</div>

<div>
<a href="#" onclick="showPage('home')">الرئيسية</a>
<a href="#" onclick="showPage('login')">الدخول</a>
</div>
</div>

<!-- الصفحة الرئيسية -->

<div id="home" class="page active home">

<h1>منصة ثانوية أبي بكر بالقايد</h1>

<p>منصة تعليمية رقمية حديثة للتواصل بين التلاميذ والإدارة</p>

<button class="btn" onclick="showPage('login')">الدخول للمنصة</button>

</div>

<!-- تسجيل الدخول -->

<div id="login" class="page">

<div class="login-box">

<h2>تسجيل الدخول</h2>

<select id="type">
<option value="student">تلميذ</option>
<option value="admin">الإدارة</option>
</select>

<input type="email" placeholder="البريد الإلكتروني">

<input type="password" id="password" placeholder="كلمة المرور">

<button class="btn" onclick="login()">دخول</button>

</div>

</div>

<!-- لوحة التلميذ -->

<div id="student" class="page">

<h1>لوحة التلميذ</h1>

<div class="card">
<h3>الدروس</h3>
<p>سيتم نشر الدروس هنا.</p>
</div>

<div class="card">
<h3>الواجبات</h3>
<p>عرض الواجبات المنزلية.</p>
</div>

<div class="card">
<h3>إرسال شكوى</h3>

<form action="mailto:Scalding2005@gmail.com">
<input type="text" placeholder="اسمك">
<textarea placeholder="اكتب الشكوى"></textarea>
<button class="btn">إرسال</button>
</form>

</div>

<a class="insta" href="https://www.instagram.com/2x_dororo?igsh=Y2tmYjJncHlwcTBo&utm_source=qr" target="_blank">
فتح حساب الانستغرام
</a>

</div>

<!-- لوحة الإدارة -->

<div id="admin" class="page">

<h1>لوحة الإدارة</h1>

<div class="card">
<h3>إدارة الدروس</h3>
<p>يمكن إضافة الدروس هنا.</p>
</div>

<div class="card">
<h3>إدارة الواجبات</h3>
<p>يمكن إضافة الواجبات للتلاميذ.</p>
</div>

</div>

<div class="footer">

تم تطوير هذه المنصة من طرف التلميذ **بن هدية محمد**  
📞 الهاتف: 0696097899

</div>

<script>

particlesJS("particles-js",{
particles:{
number:{value:90},
size:{value:3},
color:{value:"#ffd700"},
line_linked:{enable:true,color:"#ffd700"},
move:{speed:2}
}
});

</script>

</body>
</html>
