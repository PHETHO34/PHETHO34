<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Program Recommendation</title>
    <STYle>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
        margin: 20px;
        background-color: rgba(0, 0, 0,0.5);
    }
    .main{
    width: 100%;
    background: linear-gradient(to top, rgba(0,0,0,0.5)50%, rgba(0,0,0,0.5)50%),url();
    background-position: center;
    background-size: cover;
    height: 15vh;
}
.navbar{
    width: 1200px;
    height: 75px;
    margin: auto;
}
.icon{
    width:200px;
    float: left;
    height: 70px;
}
.logo{
    color:blue;
    font-size: 35px;
    font-family: Arial, Helvetica, sans-serif;
    padding-left: 20px;
    float: left;
    padding-top: 10px;
}
.menu{
    width: 400px;
    float: left;
    height: 70px;
}
ul{
    float: left;
    display: flex;
    justify-content: center;
    align-items:center;
}
ul li{
    list-style: none;
    margin-left: 62px;
    margin-top: 27px;
    font-size: 14px;
}
ul li a{
    text-decoration: none;
    color: #fff;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: bold;
    transition: 0.4s ease-in-out;
}
ul li a:hover{
    color: #ff7200;
}
    
    h1 {
        font-size: 24px;
        margin-bottom: 20px;
        color: whitesmoke;
    }
    
    form {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 20px;
        border-left: 50px;
        padding: 10px;
        margin-left: 10px;
        font-size: 30px;
        color: #fff;
        border: 1px ;
    }
    
    label input {
        color: white;
        margin-bottom: 10px;
    }
    
    button {
        background-color: #0074D9;
        color: white;
        border: none;
        padding: 10px 20px;
        cursor: pointer;
    }
    
    button:hover {
        background-color: #0056b3;
    }
    
    #program-recommendation {
        display: none;
        margin-top: 20px;
    }
    
    h2 {
        color: whitesmoke;
        font-size: 35px;
    }
    
    #program-name {
        font-size: 18px;
    }
    
.box div{
  padding: 10px;
  margin: 10px;
  float: left;
  color: #fff;
  border: 1px;
  margin-top: 75px;
}
.box div h1{
    font-size: 50px;
    font-weight: bold;
    font-family: Arial, Helvetica, sans-serif;
    padding-top: -30px;
    margin: 0%;
}
.box div p{
    font-size: x-large;
}
#kop{
  flex: 2;
  order: 2;
}
    footer{
            background-color: rgba(0, 0, 0,0.5);
            color:whitesmoke;
            padding: 5px;
            margin-bottom: 5px;
            text-align: center;
            height: 20vh;
            position: relative;
        }  
    </STYle>
</head>
<body>
    <div class="main">
        <div class="navbar">
            <div class="icon">
                <h2 class="logo">KrR</h2>
            </div>
            <div class="menu">
                <ul>
                    <li><a href="main.html">Home</a></li>
                    <li><a href="about.html">About</a></li>
                    <li><a href="index.html">Service</a></li>
                    <li><a href="design.html">Design</a></li>
                    <li><a href="events.html">Events</a></li>
                    <li><a href="#">Practicals</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="box">
        <div id="kop">
            <h1>Welcome to Limkokwing <br> University of Creative technology</h1>
            <p>
                LCGSE students are required to enter their grades to reveil the suitable <br>
                program to enroll based to the grades obtainted.
            </p> 
             <button class="cn"><a href="#">Join Us</a></button>   
        </div>
      </div>
    <h2>Program Recommend</h2>
    <form id="grade-form">
        <label for="math-grade">Math Grade:</label>
        <input type="text" id="math-grade" placeholder="Enter grade">

        <label for="science-grade">Science Grade:</label>
        <input type="text" id="science-grade" placeholder="Enter grade">

        <label for="business-grade">Business Grade:</label>
        <input type="text" id="business-grade" placeholder="Enter grade">

        <label for="english-grade">English Grade:</label>
        <input type="text" id="english-grade" placeholder="Enter grade">

        <button type="button" id="submit-button">Recommend Program</button>
    </form>

    <div id="program-recommendation">
        <img id="IMG" src="" alt="image">
        <h2>Recommended Program:</h2>
        <p id="program-name"></p>
        <p id="program-image"></p>
        <p id="program-details"></p>
    </div>
    <footer>
        <p>&copy; 2023 Limkokwing University of Creative technology. All Rights Reserved.</p>
    </footer>
    <script>
        document.querySelector('#submit-button').addEventListener('click', recommendProgram);
        
        function recommendProgram() {
            const mathGrade = document.querySelector('#math-grade').value;
            const scienceGrade = document.querySelector('#science-grade').value;
            const businessGrade = document.querySelector('#business-grade').value;
            const englishGrade = document.querySelector('#english-grade').value;
            let programName='', programImage='', programDetails='';
        
            if (mathGrade === 'A' || mathGrade === 'A*') {
                programName = 'Information Technology';
                programImage = document.getElementById("IMG");
                programImage.src="inf.jpg";
                programDetails = "A course uses computers,software,networks and technoogy. this includes hardware and software development to data management,cybersecurity and network";
            } else if (businessGrade === 'B' ||businessGrade === 'A'|| businessGrade === 'A*' && englishGrade === 'B' ||englishGrade === 'A' || englishGrade === 'A*') {
                programName = 'Business Management';
                programImage = document.getElementById("IMG");
                programImage.src="bmn.jpg";
                programDetails = "A course involves planning,organising,ordering amd managing. It encoupasses various functiond including strategic planning,finantial management,human resourses and operations";
            } else if (englishGrade === 'B' || englishGrade === 'A' || englishGrade === 'A*') {
                programName = 'Communication Studies';
                programImage = document.getElementById("IMG");
                programImage.src="bss.jpg";
                programDetails = "A course focus on various aspects of business.It provides multidisciplinary aproach, covering areas such as economics,finance,marketing,management and entrepreneurship.";
            } else {
                programName = 'SORRY! No program matches your grades.';
            }
        
            document.querySelector('#program-name').textContent = programName;
            document.querySelector('#program-image').textContent = programImage;
            document.querySelector('#program-details').textContent = programDetails;

          document.querySelector('#program-recommendation').style.display = 'block';
        }
        </script>
</body>
</html>
![bmn](https://github.com/PHETHO34/PHETHO34/assets/150231518/3bb3a77e-24dc-4595-9275-ed0168d81b07)
