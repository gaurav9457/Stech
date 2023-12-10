<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Responsive Form</title>
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN"
      crossorigin="anonymous"
    />
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Chakra+Petch:wght@300&family=Lora&family=Orbitron&family=Roboto+Slab&family=Ubuntu:wght@300&display=swap" rel="stylesheet">
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"
      integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL"
      crossorigin="anonymous"
    ></script>
    <style>
        body{
            background-image: url(https://media.istockphoto.com/id/1371310881/vector/light-blue-turquoise-color-gradient-defocused-blurred-motion-abstract-background-vector.jpg?s=612x612&w=0&k=20&c=zBkkyu7Jjmjkvnc1AmUDJekeP_yv2Q_dY2cESoqWcQ0=);
            background-repeat: no-repeat;
            background-size: cover;
            
        }
        h5{
         font-family: 'Roboto Slab', serif;
        }
        .popup {
            display:none;
            position:fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: grey;
            text-align: center;
        }
        .popup-content {
            position: relative;
            /* top: 50%; */
            /* transform: translateY(-50%); */
            background-color: black;
            color: white;
            width: 80%;
            max-width: 450px;
            margin: 0 auto;
            padding: 20px;
            border-radius: 5px;
        }
        .close {
            position: absolute;
            top: 10px;
            right: 10px;
            cursor: pointer;
        }
    </style>
  </head>
  <body>
    <!----------------- NavBar ---------------- -->
    <div class="container-fluid bg-info">
     
      <div class="container-fluid">
      <nav class="navbar navbar-expand-md  bg-info ">
        <div class="container">
          <a class="navbar-brand" href="http://127.0.0.1:5500/Task1.html#" style="color: white;">Employee_Registration </a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarScroll" aria-controls="navbarScroll" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarScroll">
            <ul class="navbar-nav me-auto my-2 my-lg-0 navbar-nav-scroll" style="--bs-scroll-height: 100px;">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="http://127.0.0.1:5500/Task1.html#">Home</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#">About</a>
              </li>
             
            </ul>
            <form class="d-flex" role="search">
              <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
              <button class="btn btn-outline-success" type="submit">Search</button>
            </form>
          </div>
        </div>
      </nav>
    </div>
      
    </div>

    <!-- -----------Form-------------- -->
    <div class="container mt-2" >
      
         <form action="" id="EmployeeData" >
              <div class="row mx-md-5">
            <h5 class="mt-3">Personal Information :</h5>
            <div class="col-md-8 mx-md-5">
               
                <label for="fname" class="form-label">Full_Name</label>
                <input
                  type="text"
                  id="fname"
                  class="form-control" placeholder="Enter Your FullName" autofocus />
                  
                
                  <label for="flexRadioDefault1" class="form-label">Gender</label>
              
                  <div class="form-check">
                    <input type="radio" id="gender" name="gender" value="Male"> <label for="male">Male</label>
                
                    <!-- <label class="form-check-label" for="flexRadioDefault1">
                     Male
                    </label> -->
                    
                  </div>
                  <div class="form-check">
                    <input type="radio" id="gender" name="gender" value="Female"> <label for="female">Female</label>
                    <!-- <label class="form-check-label" for="flexRadioDefault2">
                      Female
                    </label> -->
                  </div>
                  <label for="dob">Date Of Birth :</label>
              <div class="row mt-2">
                <div class="col-md-4">
              <input type="date" name="" id="dob" required> 
            </div>
        </div>
        

    </div>

    <h5 class="mt-3">Contact Details :</h5>
    <div class="col-md-8 mx-md-5">
               
        <label for="hno" class="form-label">Address</label>
        <input
          type="text"
          id="hno"
          class="form-control" placeholder="House No "/>
        <div class="row">
            <div class="col-md-4 form-floating mt-2">
          <!-- <label for="Street" class="form-label">Street Name</label>
        <input
          type="text"
          id="Street"
          class="form-control" placeholder="Street"/> -->
          <input type="text" class="form-control" id="Street" placeholder="">
          <label for="Street">Street</label>
        </div>
        <div class="col-md-4 form-floating mt-2">
          <!-- <label for="City" class="form-label">City</label>
        <input
          type="text"
          id="City"
          class="form-control" placeholder="City"/> -->
          <input type="text" class="form-control" id="City" placeholder="">
          <label for="City">City</label>
        </div>
        <div class="col-md-4 form-floating mt-2">
          <input type="number" class="form-control" id="zip" placeholder="">
          <label for="City">Zipcode</label>
          
        </div>
        </div>
          <label for="state" class="form-label">State</label>
          <input
            type="text"
            id="state"
            class="form-control" placeholder="State"/>

          </div>
          
     <h5 class="mt-3">Employment Details</h5>   
     <div class="col-md-8 mx-md-5">
               
        <label for="jTitle" class="form-label">Job Title</label>
        <input
          type="text"
          id="jTitle"
          class="form-control" placeholder="Enter Job Title"/>
        
          <label for="Department" class="form-label">Department</label>
        <input
          type="text"
          id="Department"
          class="form-control" placeholder="Department"/>
          <label for="Empid" class="form-label">Employee Id</label>
        <input
          type="text"
          id="Empid"
          class="form-control" placeholder="Empid"/>
          

    </div> 

    <h5 class="mt-3" >Education Details</h5> 
    <div class="row col-md-8 mx-md-5">
      <div class="col-md-4">
        <label for="Passout" class="form-label">Passout Year :</label>
        <input type="number" class="form-control" id="Passout"/>
      </div>
      <div class="col-md-4">
        <label for="Marks" class="form-label">Marks</label>
        <input
          type="number"
          id="Marks"
          class="form-control" placeholder="Enter Marks"/>
      </div>
      <div class="col-md-4">
        <label for="field" class="form-label">Field</label>
        <input
          type="text"
          id="field"
          class="form-control" placeholder="Enter Field"/>
      </div>
          
    </div> 


    <div class="col-md-6 mx-md-auto d-flex justify-content-between">
    <button class="btn btn-success btn-lg mt-3" type="Submit" value="Submit" onclick="return validInp()">Submit</button>
    <button class="btn btn-outline-danger btn-lg mt-3" type="" value="Cancle" onclick="reset()">Cancle</button>
     </div>
         </div>
         </form>
</div>

      <!-- ----------Footer------------- -->
     <div class="container-fluid bg-secondary   mt-4">
        <footer class="py-3 my-4">
            <ul class="nav justify-content-center border-bottom pb-3 mb-3">
              <li class="nav-item"><a href="http://127.0.0.1:5500/Form.html?" class="nav-link px-2 text-muted">Home</a></li>
              <li class="nav-item"><a href="#" class="nav-link px-2 text-muted">Features</a></li>
              <li class="nav-item"><a href="#" class="nav-link px-2 text-muted">Pricing</a></li>
              <li class="nav-item"><a href="#" class="nav-link px-2 text-muted">FAQs</a></li>
              <li class="nav-item"><a href="#" class="nav-link px-2 text-muted">About</a></li>
            </ul>
            <p class="text-center text-muted">© 2022 Company, Inc</p>
          </footer>
     </div>

     <div id="popup" class="popup">
        <div class="popup-content">
            <span class="close" onclick="closePopup()">&times;</span>
            <h2>Employee data Submitted</h2>
            <div id="popup-content"></div>
        </div>
    </div>



</div>
      <!-- </div> -->
    </div>
   
    <script>
         
         function validInp() {
          const firstName = document.getElementById('fname').value;
          const hno =document.getElementById('hno').value;
          const Passout =document.getElementById('Passout').value;
          const Marks =document.getElementById('Marks').value;
          const field =document.getElementById('field').value;

          if(firstName.length !=0 && hno.length !=0 ){
                  alert("Form Submitted");
                  submitForm();
                }
                else {
                  
                  alert("Fill all details (Fullname, Address, Passout Year, Marks, Field)");
                }
          
         }
         function submitForm() {
            
            const firstName = document.getElementById('fname').value;
            const gender = Array.from(document.querySelectorAll('input[name="gender"]:checked')).map(e => e.value);
            // const gender=document.getElementById('gender').value;
            const dob = document.getElementById('dob').value;
           
            const hno =document.getElementById('hno').value;
            const Street =document.getElementById('Street').value;
            const City =document.getElementById('City').value;
            const Zip =document.getElementById('zip').value;

            const jTitle =document.getElementById('jTitle').value;
            const Department =document.getElementById('Department').value;
            const Empid =document.getElementById('Empid').value;

            const Passout =document.getElementById('Passout').value;
            const Marks =document.getElementById('Marks').value;
            const field =document.getElementById('field').value;
           
            
            const popupContent = `
                <p><b>First Name:</b> ${firstName}</p>
                <p><b>Gender:</b> ${gender}</p>
                <p><b>Date of Birth:</b> ${dob}</p>
                <p><b>Address :</b> ${hno}</p>
                <p><b>Street :</b> ${Street}</p>
                <p><b>City :</b> ${City}</p>
                <p><b>Zipcode :</b> ${Zip}</p>
                <p><b>Job Title:</b> ${jTitle}</p>
                <p><b>Department:</b> ${Department}</p>
                <p><b>Employee Id:</b> ${Empid}</p>
                <p><b>Passout Date:</b> ${Passout}</p>
                <p><b>Marks :</b> ${Marks}</p>
                <p><b>field:</b> ${field}</p>
                `;
               
               
            const popup = document.getElementById('popup');
            const popupContentDiv = document.getElementById('popup-content');
            popupContentDiv.innerHTML = popupContent;
            popup.style.display = 'block';

            document.getElementById('EmployeeData').reset();
            
            const StoreData={
              firstName : firstName,
              gender : gender,
              dob :dob,
              hno :hno,
              Street :Street,
              City :City,
              Zip:zip,
              jTitle :jTitle,
              Department :Department,
              Empid :Empid,
              Passout :Passout,
              Marks :Marks,
              field :field

            }
            localStorage.setItem("Name",JSON.stringify(StoreData));
            return false; 
        }

         
        function closePopup() {
            
            const popup = document.getElementById('popup');
            popup.style.display = 'none';
            const popupContentDiv = document.getElementById('popup-content');
            popupContentDiv.innerHTML = '';
        }

         
    </script>
    <script
      src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js"
      integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r"
      crossorigin="anonymous"
    ></script>
    <script
      src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.min.js"
      integrity="sha384-BBtl+eGJRgqQAUMxJ7pMwbEyER4l1g+O15P+16Ep7Q9Q+zqX6gSbd85u4mG4QzX+"
      crossorigin="anonymous"
    ></script>
  </body>
</html>
