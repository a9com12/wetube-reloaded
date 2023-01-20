form {
max-width: 420px;
margin: 0 auto;
&:not(.search\_\_form) {
padding: 30px;
background-color: rgba($color: $bg, $alpha: 0.7);
    border-radius: 10px;
    border: 1px solid rgba($color: #fff, $alpha: 0.1);
}
}

input {
all: unset;
padding: 15px 20px;
border-radius: 5px;
border: 1px solid rgba(255, 255, 255, 0.2);
background-color: black;
margin-bottom: 5px;
font-size: 16px;
color: white;
width: 90%;
&::placeholder {
color: rgba(255, 255, 255, 0.7);
}
}

input[type="submit"],
.social\_\_btn {
border-radius: 5px;
padding: 12px 20px;
background-color: white;
color: rgba($color: $red, $alpha: 1);
text-align: center;
cursor: pointer;
display: block;
}
