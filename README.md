# Build-a-Survey-Form

 
 
<style> 
 
.container{
display:grid;
grid-template-columns: 100%;
grid-template-rows: 75px 1700px;
grid-template-areas: 
"banner" 
"body";
}
 
.banner{
display:grid;
grid-template-areas:
"bannerleft bannerright";
grid-template-columns: 1fr 1fr; 
background:black;
height: 75px;
width:100%;
}
 
.bannerleft{
display:grid;
grid-template-areas:
"diamond FCC";
grid-template-columns: 85px 215px;
}
 
.diamond{
background-color:white;
height: 85px;
}
 
.FCC{
color:white;
display:grid;
width:300px;
grid-template-areas:
"Survey"
"free";
grid-template-columns: 450px;
grid-template-rows: 20px 20px;
}
 
.Survey{
width:100%;
font-size:22px;
padding: 12 0 0 5;
}
 
 
.free{
padding:21 0 0 5;
color:white;
}
 
.Follow{
background: green;
width:60px;
height:20px;
border-radius:2px;
margin: 0 0 0 135;
padding:2 0 0 5;
font-size:15px;
text-decoration:none;
color:white;
 
}
 
.bannerright{
display:grid;
grid-template-areas:
"Like View Sign Log";
"diamond FCC";
grid-template-columns: 70px 145px 120px 90px;
Justify-content:right;
margin:11 10 20 0; 
color:white;
 
}
 
.Like{
background-color: green;
display:flex;
justify-content:flex-end;
width:60;
border-radius:4px;
display: flex;
align-items: center;
text-decoration:none;
color:white;
 
}
 
 
 
.View{
background-color: gray;
width:135;
border-radius:4px;
display: flex;
align-items: center;
text-decoration:none;
color:white;
}
 
.Sign{
background-color: green;
width:110;
border-radius:4px;
display: flex;
align-items: center;
text-decoration:none;
color:white;
}
 
.Log{
background-color:gray;
border-radius:4px;
display: flex;
align-items: center;
text-decoration:none;
color:white;
}
 
 
.body{
display:grid;
grid-template-rows:150px 1700px;
grid-template-columns:100%; 
grid-template-areas:
"header"
"main";
background:darkblue;
height:1700px;
text-align:center;
 
}
 
.header{
margin: 50 0 0 0;
background:darkblue
}
 
.main{
display:grid;
grid-template-columns: 1fr 1fr 1fr;
grid-template-rows: 
1500px;
grid-template-areas:
"c1 c2 c3";
height:1550px;
 
 
}
 
.c1{
display:grid;
background:darkblue;
position: relative;
 
}
.c2{
display:grid;
grid-template-areas:
"name"
"email"
"age"
"Which"
"would"
"what1"
"what2"
"any"
"submit";
height:1550px;
background:black;
color:white;
width:800px;
position: relative;
justify-content: center;
font-size:20;
 
}
 
.name{
padding: 0px 0 0 15;
margin: 0 0 0 0;
width:80%;
height: 45px;
placeholder: "Enter your name"      
border-style: solid;
border-radius: 10px; 
}
 
.email{
padding: 0px 0 0 15;
margin: 0px 0 0 0;
width:80%;
height: 45px;
 
border-style: solid;
border-radius: 10px; 
} 
 
.age{
padding: 0px 0 0 15;
margin: 0px 0 0 0;
width:80%;
height: 45px;
border-style: solid;
border-radius: 10px; 
 
}
 
.Which{
padding: 0px 0 0 15;
margin: 0px 0 0 0;
width:80%;
height: 45px; 
border-style: solid;
border-radius: 10px;  
color:gray;
}
 
.would{
padding: 0px 0 0 15;
margin: 0px 0 0 0;
width:80%;
height: 45px;
 
border-style: solid;
border-radius: 10px;  
}
 
.what{
padding: 0px 0 0 15;
margin: 0px 0 0 0;
width:80%;
height: 45px;
color:gray;
border-style: solid;
border-radius: 10px;  
}
 
.what2{
}
 
.c3{ 
background:darkblue;
position: relative;
} 
 
.any{
padding: 0px 0 110 15;
margin: 0px 0 0 0;
width:80%;
height: 160px;    
border-style: solid; 
}
 
.submit{
background-color:green;
color:white;
width: 80%;
height: 50px;
}
 
 
</style> 


<!DOCTYPE html>
<html>
 
<div class= "container">
 
<div class="banner"> 
 
<div class="bannerleft">  
<img class="diamond" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAANgAAADpCAMAAABx2AnXAAAAwFBMVEUxmc7///8REiQrg7IOAAszmMwllcyNv94sl82fyuRhqtP8//4AAAAODyJWptMmlswAABcAABoAABQYksvx9/rF3+0AABgGCB5bW2SmzuRor9aBu9yWxuBFoNBvs9fs9fjP5fBnaHGUlJre7PSz1OkXGCkjJTOcnKCCgorV1dlBQUwAAB86OkaVlJwAAA4hIjCGh45lZW+92us0M0Cqq65xcXhNUFnr6+vDxcg/QU/e3uHCwsS1trcoKTOgoKaEhI1D8MsqAAAIZElEQVR4nO2cC3uiOBSGgV0oVVABW6jVWvFSZFSwNkynO9r//68WSFAuidhnO0C75+0zU+Xi5OPk9p3E4TgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAL4ZchrqwfzZ9CFJZnxs7UidVhpSzg4VfE7O3NBpqDSp1eZT3EnxwWu+TYG/xmfv0ne0W1K9CuhIg4yuvhEdlMXMwZQIMY6O0c8cHUhivSIo5HTxV/HTN2Z0XTw/i4VLV1m5g8bFzMjWQ37ajQ+PWLp4fhRf0J1mlTWtNnZz8eIfYmHGM1vYMw7ZQ+5ws5Tl+g2ef8QtrMNoYXFwOriVPeYON6k2Sp18qXFfb9ywdfH8DRFfENwYZYV4JWVundPFVN8YZQVd7faIWsvyTLH8Uf6xNKMHEaViQ5rh0XdwXlc0bEXXGXf542HM6h/PukVdfTL4TvMnCiGLhcliP3+i3enWq4qqix/igN2X6eL5e3zlsHCi3apZGaUe8mMch25pwJKQcca4qKzeHoQWryQMFwTs3LW1KqPF6xiFQsOhgafKnESJbo3KpA6t8APccxTbDZUhuwPt16VMKgxAEXgyxXEXBSwsfXyxKNGGvP6oFmXUesjzZAZYGJtY3NEnVjF11Ea5S62HZM4uUoNJpY3tC90H1FAbpRG9ruGzbH9ZBDtOTqSerLw20vsNnqQyzvnLIjhk0jVdWbUxY9RDfixeYFfyECvAFUdprKzCOQirHpJEB70nYIP7m1z646SsutrYZekak+G2xK7keTRwnOkhC5VVFDOmLv4BB6zUruQZxCXv5tMfJ2XVxIyZyJiy50fnSWZhrBtJeuSPIzLg8D8vj1gXsBiRcsvMKyrRxaVWHDKHT+c/+nmFj2B8MgD8L5AlBklTYJ1nc+kn/1ldreEVnQHpFa9LGJ4gd+IbuwPGBw9blSiTWDPBPn7y0sVeLGFGbmQN/DfVDNAy05QMWXnC8/TxOEbJwmV0V6GMEZPQ50dDqUF3IExiEy0yswl3hlxZXphVdOzzuS5jOst4HN2z2YRroypVXBQzerUhPp/lQOgMiTmlT0GHVeoKMej50BkztcuEdDmMhntfsa6wIHSTQfqBi9LApOiRMFGmZxMeKtcVKaPVnZuPWheyCk/NJrTr0EVbyIzA1olpGgvcn8km1LUASE1VPeI1u7LVzARsTkXa5bWluKMkAaWTIPmBkvXnBDwNK2yKCBlXleq4VFni8y8K2SOzSY7rSdwnyFyxSDhk3EU5uE5cbykBm9ZtmynKSBLu3K6cBDy7FYvDXu26otWJQp1L0qblCxOsVOljt3ZdkTvMD0FjXKrylYlnRnL7xmiArmjimK90Q7JNo0wYvr8w73xuyk7TgkEjGz3KHGeygJQbDSuzXxeQtxx422yhyHn59HtrmUYxEPPVCZeZseZFuCaba7NHh0b9u43SGNmeLekWzoQs2ZiUbaBXTYpXTNagtc+vecWhoQ0K1duvcrI2htgXtuPs04bxemxKGUZmX3CnxHFiu9JNT7zag0bqCkfqtEEj01vWVrHEX6amLc3Yf0kls+aON+bRDElc6XDAUuamRvtVTnoVl6xv0u3LlNjRUzxr2l90KWmD9nBmA21h1blWW3kJsngMwhnHWWiAU7Eh00M2KYPGztO04tXZU5c5bdZsg87JoPXx7KiYWUsGuaRBPja8GhLkoxKcnhYLIetk92pWtEr0CSTTiT5Hmw6GE8kokseJ5HMzh2UaR4NGdlnm0tdk5YLYldnX0cUdS518FyRjuWapb360m2W/LoA0oCQcqblWm1wwI82w8f18DmLQSMhSjhPv1STVs+rVr88AGzSyy/KUJEg6lLjnbKL9KgevoHVyC+fD1KjdTPtVjhRZT/KlRonMIccnu9KoLy1+jPirtoOM4yT+chDZr4albT5CtII2TScJkrz+tNpNzJ+PFNoY4injFnefuM+aV4n+O6FBG5/WwI7fFxuPvtrwVUDmxlfHdoX9pXQ1br79KkfmbuLwyMZ0Gk8z5NFN/atfn4E8wv97hzzAHaTc+vr1MAH368mmZrm6TV8AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAANTMX98U7u9vCid8U0DYV4MIU8kfIfVbEExTUFPvwlPm6W3DwcLUlSqo+zl+vZuTcz3L0verRMo8MNWFtfsqyrAwbbLVen5P7wm3uuLPTV2/NXXlJQQ9KbqimKai7JaKsnr/ZdZc4CL0R00i5vm65yDbURwbOeudbSP3ELwFijL5adnL5cJdLoNXd7n4tao4YmHdD3/U+G/t+E6N5ODj0YM2TXOuqlr469RySBvT7fkEoR5CE0Xxf9iCgpC1cZdvodjFUtm+/LNSFj+X4a3V6jKt1cRb6Iv5qrfX1Inj7s2FNneDuWrutfCV4PUmv9YLy0HO/h0h33WCtWumhWmW5VvrbXirqfvq06Y38QNzo/x4c+zgt7L6/brZ7H8uvarroSr4jnNAjmUjhGzLmSDHCfztIdj4oRh0ePJ3aHPYWbZlzy2k+mtni5xeWphqvjieby4WtupZW2QJthVoT8h//fW2W6J/kP3bcV/dt03FwgT9ED5whALHsdZWgN6R72z9yTuaH9z11neQhYJQoX8I7O3ae1k5k7W11tPCBA155t5H5sJHm60y8b3dzgxs51a3gh+2pW/CKokUVHULE9S50HN7K29huponuL2dsNJ3O2EXvXe1hTdfCd5K1xfezgvcIBBcndTE0wCthW3xVhPUniaEP724Xeq3qqCZqq6Fp/Ww7WrV9/VqNH7iTkIlr1SVdCa4G4l7khAz6jvMYx/53Wce3w8Q9tX4F7+rzQvMOqbBAAAAAElFTkSuQmCC">   
<div class="FCC"> 
<div class="Survey"> FCC:Survey Form </div>  
<a href="freeCodeCamp.org" class="free"> freeCodeCamp.org </a> 
<a href="https://codepen.io/Login?" class="Follow"> +Follow </a> 
 
</div>  
</div> 
 
<div class="bannerright"> 
<a href="https://codepen.io/Login?" class="Like"> <div style="padding: 0 15 0 0;"> Like </div> </a> 
<a href="https://codepen.io/freeCodeCamp/pen/VPaoNP" class="View"> <div style="padding: 0 0 0 16;"> View in Editor</div> </a> 
<a href="https://codepen.io/accounts/Signup/user/free"class="Sign"><div style="padding: 0 0 0 25;"> Sign Up </div> </a> 
<a href="https://codepen.io/Login"class="Log"> <div style="padding: 0 0 0 25;"> LogIn </div> </a> 
</div> 
 
</div>   
 
<div class="body"> 
<div class="header">
<div style="font-size:30px;color:white;font-size:40"> freeCodeCamp Survey Form </div> 
<div style="padding:0 0 0 0;font-size:20;color:white">Thank you for taking the time to help us improve the platform </div> 
</div>
 
<div class="main"> 
<div class="c1">  </div>
<div class="c2">
<div style= "color: white; padding:0 650 0 0; margin:50 0 0 0;"> Name </div>
<form style="width:875; margin:0 0 0 0">  <input placeholder="Enter your name" class="name" type="text">   </form>  
<div style= "color: white; padding: 15 650 0 0";> Email </div> 
<form>  <input placeholder="Enter your email" class="email" type="text"> </form> 
<div style= "color: white; padding: 0 575 0 0";> Age (optional) </div> 
<form>  <input placeholder="age" class="age" type="text">  </form>
<div style= "color: white; padding: 0 320 0 0";  > Which option best describes your current role? </div> 
<form>
<select class="Which">
<option> Select current role</option>            
<option>Student</option>
<option>Full Time Job</option>
<option>Full Time Learner</option>
<option>Other</option>
</select>
</form>
<div style="padding: 20 200 0 0;";> Would you recommend freeCodeCamp to a friend? (optional)  
<form style="padding:20 395 0 0;"> 
<input class="Definetly" type="radio"> Definetly 
</form>
<form style="padding:0 415 0 0;"> 
<input class="Maybe" type="radio" > Maybe 
</form>
<form style="padding:0 400 0 0;"> 
<input class="Not-sure" type="radio"> Not sure 
</form>
</div>
<div style= "padding:0 300 0 0"> What is your favorite feature of freeCodeCamp?  </div>       
<form type="dropdown">  
<select class="what">
<option> Select an option </option> 
<option> Challenges </option> 
<option> Projects </option> 
<option> Open source </option> 
</select>  
</form> 
<div style= "padding: 20 190 0 0"> What would you Like to see improved? (Check all that apply) 
<form style="padding: 20 325 0 0" > <input type="checkbox"> Front-end projects </form>     
<form style="padding: 0 328 0 0"> <input type="checkbox"> Back-end projects  </form>  
<form style="padding: 0 324 0 0"> <input type="checkbox"> Data Visualization  </form> 
<form style="padding: 0 380 0 0"> <input type="checkbox"> Challenges  </form>
<form style="padding: 0 264 0 0"> <input type="checkbox"> Open Source Community  </form>
<form style="padding: 0 326 0 0"> <input type="checkbox"> Gitter help rooms  </form>
<form style="padding: 0 410 0 0"> <input type="checkbox"> Videos  </form>
<form style="padding: 0 355 0 0"> <input type="checkbox"> City Meetups  </form>
<form style="padding: 0 422 0 0"> <input type="checkbox"> Wiki  </form>
<form style="padding: 0 405 0 0"> <input type="checkbox"> Forum  </form>
<form style="padding: 0 305 0 0"> <input type="checkbox"> Additional Courses</form>
</div> 
<div style= "color: white; padding: 0 440 0 0";> Any comments or suggestions? </div> 
<form>  <input placeholder="Enter your comments here..." class="any" type="text"> 
</form>
<form action="mailto:youremail@youremail.com">
<input type="submit" class="submit"> 
</form> 
</div> 
<div class="c3">  </div>
 
</div>
</div>
</div> 
</div> 
 
</html>
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 

