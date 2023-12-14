 <div class="tab-pane fade" id="nav-disabled" role="tabpanel" aria-labelledby="nav-disabled-tab"
                        tabindex="0">
                        <div class="accordion mt-5" id="accordionExample">
                            <div class="accordion-item">
                              <h2 class="accordion-header">
                                <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                                 Recent Employment Details
                                </button>
                              </h2>
                              <div id="collapseOne" class="accordion-collapse collapse show" data-bs-parent="#accordionExample">
                                <div class="accordion-body">
                                    <div class="row">
                                        <div class="col">
                                            <label for="">Company Name : <span style="color: red;">*</span></label>
                                            <input type="text" class="form-control" placeholder="Enter Company name"
                                                aria-label="First name" id="Company">
                                        </div>
                                        <div class="col">
                                            <label for="">Location :</label>
                                            <input type="text" class="form-control" placeholder="Location"
                                                aria-label="Last name" id="Location">
                                        </div>
                                    </div>
                                    <div class="row">
                                      <div class="col">
                                          <label for="">Job Title :<span style="color: red;">*</span></label>
                                          <input type="text" class="form-control" placeholder="Title"
                                              aria-label="First name" id="jTitle">
                                      </div>
                                      <div class="col">
                                        <select class="form-select form-select-md mt-4" id="Experience" aria-label="Large select example">
                                            <option selected>Year of Experience</option>
                                            <option value="Single">Less than 1 year</option>
                                            <option value="Married">2 Years</option>
                                            <option value="Divorced">4 Years</option>
                                          </select>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                            <div class="accordion-item">
                              <h2 class="accordion-header">
                                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                                  Previous Employment Details
                                </button>
                              </h2>
                              <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                                <div class="accordion-body">
                                  <div class="row">
                                    <div class="col">
                                        <label for="">Company Name :<span style="color: red;">*</span></label>
                                        <input type="text" class="form-control" placeholder="Enter Company name"
                                            aria-label="First name" id="PCompany">
                                    </div>
                                    <div class="col">
                                        <label for="">Location :</label>
                                        <input type="text" class="form-control" placeholder="Location"
                                            aria-label="Last name" id="PLocation">
                                    </div>
                                </div>
                                <div class="row">
                                  <div class="col">
                                      <label for="">Job Title :<span style="color: red;">*</span></label>
                                      <input type="text" class="form-control" placeholder="Title"
                                          aria-label="First name" id="PjTitle">
                                  </div>
                                  <div class="col">
                                    <select class="form-select form-select-md mt-4" id="PExperience" aria-label="Large select example">
                                        <option selected>Year of Experience</option>
                                        <option value="Less than 3 year">Less than 3 year</option>
                                        <option value="5 Years">5 Years</option>
                                        <option value="7 Years">7 Years</option>
                                      </select>
                                </div>
                              </div>
                              <div class="row">
                                <div class="col">
                                    <label for="">Technology Used :</label>
                                    <input type="text" class="form-control" placeholder="Technology used seperated by comma,"
                                        aria-label="First name" id="PTechnology">
                                </div>
                              </div>
                                </div>
                              </div>
                            </div>
                           
                          </div>
                          <div class="col-md-6 mx-md-auto d-flex justify-content-between">
                            <button class="btn btn-info btn-lg mt-3" type="Submit" value="Submit"
                                onclick="Employment()">Submit</button>
                            <button class="btn btn-outline-danger btn-lg mt-3" type="" value="Cancle"
                                onclick="clearEmployment()">Cancle</button>
                        </div>
                    </div>


                    function Employment() {
          let employmentArray= localStorage.getItem('Employment')? JSON.parse(localStorage.getItem('Employment')):[];

          var employment={
            Company:   document.getElementById("Company").value,
            Location:  document.getElementById("Location").value,
            jTitle:    document.getElementById("jTitle").value,
            Experience:document.getElementById("Experience").value,

            PCompany:   document.getElementById("PCompany").value,
            PLocation:  document.getElementById("PLocation").value,
            PjTitle:    document.getElementById("PjTitle").value,
            PExperience:document.getElementById("PExperience").value,
            PTechnology: document.getElementById("PTechnology").value
          }
          employmentArray.push(employment);
          localStorage.setItem('Employment',JSON.stringify(employmentArray));
          clearEmployment();
          
        }
