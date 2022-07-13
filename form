<!DOCTYPE html>
<html>
<head>
        <meta charset="utf-8">
        <meta name ="viewport",content="width=device-width,initial-scale=1.0">
        <meta http-equiv="X-UA-Compatible" content="ie=edge">
        <title>JS form validation</title>
        <style>
            body{
                padding:10px 50px;
                background:rgb(93, 168, 187);
                 color:rgb(35, 19, 80);
            }
            h1
            {
                color:#09385a;
                
            }
            .fromdesign
            {
                font-size:20px;
               
                background-color: #7e8d29;
            }
            .formdesign input{
                border:1px solid lightgreen;
                background-color:lavender;
                border-radius:4px;
                font-size:15px;margin:14px;
            }
            .fromerror{
                color:red;
            }
            .but
            {
                border-radius: 9px;
                width: 90px;
                height: 50px;
                font-size: 25px;
                margin: 22px 20px;
                background: #226899;
            }

        </style>

</head>    
<body>
<center>
<h1>Welcome to Js form</h1>

<form action="/myaction.php" name="myform" onsubmit="return validateForm()" method="post">
    <div class="formdesign" id="name">
    Name: <input type="text"name="fname" required><span class="fromerror"><b></b></span>
    
    </div>
    <div class="formdesign" id="email">
    Email: <input type="email"name="femail" required><span class="fromerror"><b></b></span>
    
    </div>
    <div class="formdesign" id="phone"required>
    Phone: <input type="phone"name="fphone"required><span class="fromerror"><b></b></span>
    
    
    <div class="formdesign" id="pass"required>
    Password: <input type="password"name="fpass"required><span class="fromerror"><b></b></span>
    </div>
    
    <div class="formdesign" id="cpass">
    Confirm Password: <input type="text"name="fcpass"required>
    <span class="fromerror"><b></b></span>
    </div>
    
    <input type="Submit" class="but" value="submit">
</form>
</center>
</body>
<script>
    function clearErrors(){

        errors=document.getElementsByClassName('fromerror');
        for(let item of errors)
        {
            item.innerHTML="";
        }
    }
function seterror(id,error){
    //sets error inside tag of id
    element=document.getElementById(id);
    element.getElementsByClassName('fromerror')[0].innerHTML=error;
}
function validateForm(){
    var returnval=true;
    clearErrors();
    var name=document.forms['myform']["fname"].value;
    if(name.length<5){
        seterror("name","Length of name is too short");
        returnval=false;
    
    }

    if(name.length==0){
        seterror("name","Enter your name");
        returnval=false;
    }
    var email=document.forms['myform']["femail"].value;
    if(email.length>20){
    seterror("email","enter valid email");
    returnval=false;
    }
    var phone=document.forms['myform']["fphone"].value;
    if(phone.length!=10){
    seterror("phone","enter valid phone number");
    returnval=false;
    }
    var pass=document.forms['myform']["fpass"].value;
    if(pass.length<6){
    
    seterror("pass","Password must be atleast 6 charecters");
    returnval=false;
    }
    var cpass=document.forms['myform']["fcpass"].value;
    if(cpass!=pass){
    
    seterror("cpass","Password and confirm password should be matched");
    returnval=false;
    }

return returnval;
}

</script>
</html>
