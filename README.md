# form.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WD101-Form</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="script.js"></script>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <section class="h-full gradient-form bg-gray-200 md:h-screen">
        <div class="container py-12 px-8 h-full">
          <div class="flex justify-center items-center flex-wrap h-full g-6 text-gray-800">
            <div class="xl:w-10/12">
              <div class="block bg-white shadow-lg rounded-lg">
                <div class="lg:flex lg:flex-wrap g-0">
                  <div class="lg:w-5/12 px-4 md:px-0">
                    <div class="md:p-12 md:mx-6">
                      <div class="text-center">
                        
                        
                      </div>
                      <form id="form" onsubmit="return submitDetails();">
                        <p class="mb-4">Please submit your details!</p>
                        <div class="mb-4">
                          <input
                            type="text"
                            class="form-control block w-full px-3 py-1.5 text-base font-normal text-gray-700 bg-white bg-clip-padding border border-solid border-gray-300 rounded transition ease-in-out m-0 focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none"
                            id="name"
                            placeholder="Name"
                            name="name"
                            required
                          />
                        </div>
                        <div class="mb-4">
                            <input
                              type="email"
                              class="form-control block w-full px-3 py-1.5 text-base font-normal text-gray-700 bg-white bg-clip-padding border border-solid border-gray-300 rounded transition ease-in-out m-0 focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none"
                              id="email"
                              placeholder="Email"
                              name="email"
                              required
                            />
                        </div>
                        <div class="mb-4">
                          <input
                            type="password"
                            class="form-control block w-full px-3 py-1.5 text-base font-normal text-gray-700 bg-white bg-clip-padding border border-solid border-gray-300 rounded transition ease-in-out m-0 focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none"
                            id="password"
                            placeholder="Password"
                            name="password"
                            required
                          />
                        </div>
                        <div class="mb-4">
                            <input
                              type="text" 
                              onfocus="(this.type='date')"
                              onfocusout="(this.type='text')"
                              class="form-control block w-full px-3 py-1.5 text-base font-normal text-gray-700 bg-white bg-clip-padding border border-solid border-gray-300 rounded transition ease-in-out m-0 focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none"
                              id="dob"
                              placeholder="Date of Birth"
                              name="dob"
                              required
                            />
                        </div>
                        <div class="mb-4">
                            <input
                                type="checkbox"
                                class="form-control px-3 py-1.5 text-base font-normal text-gray-700 bg-white bg-clip-padding rounded transition ease-in-out m-0 focus:text-gray-700 focus:outline-none"
                                id="terms"
                                name="terms"
                            />
                            <label 
                                for="terms" 
                                class="form-control ml-2 text-base font-normal text-gray-700 bg-white bg-clip-padding rounded transition ease-in-out m-0 focus:text-gray-700 focus:outline-none"
                            >You agree to the terms and conditions.</label>
                          </div>
                        <div class="text-center pt-1 mb-12 pb-1">
                          <button
                            class="inline-block px-6 py-2.5 text-white font-medium text-xs leading-tight uppercase rounded shadow-md hover:bg-blue-700 hover:shadow-lg focus:shadow-lg focus:outline-none focus:ring-0 active:shadow-lg transition duration-150 ease-in-out w-full mb-3"
                            type="submit"
                            style="
                              background: linear-gradient(
                                to right,
                                #ee7724,
                                #d8363a,
                                #dd3675,
                                #b44593
                              );
                            "
                          >
                            Submit Details
                          </button>
                        </div>
                        <div class="flex items-center justify-between pb-6">
                          
                         
                        </div>
                      </form>
                    </div>
                  </div>
                  <div
                    class="lg:w-7/12 flex items-center lg:rounded-r-lg rounded-b-lg lg:rounded-bl-none"
                    
                  >
                    <div class="text-white px-4 py-6 md:p-12 md:mx-6">
                      
                        <h4 class="text-xl font-semibold mb-6">Data registered:</h4>
                        <div class="flex flex-col">
                            <div class="overflow-x-auto sm:-mx-6 lg:-mx-8">
                              <div class="py-2 inline-block min-w-full sm:px-4 lg:px-6">
                                <div class="overflow-hidden">
                                  <h2 id="nodata" class="text-2xl font-bold text-center hidden px-6">There is nothing here yet!</h2>
                                  <table class="min-w-full hidden" id="table">
                                    <thead class="bg-gray-400 border-b">
                                      <tr>
                                        <!-- <th scope="col" class="text-sm font-medium text-gray-900 px-4 py-3 text-left">
                                          #
                                        </th> -->
                                        <th scope="col" class="text-sm font-medium text-gray-900 px-4 py-3 text-left">
                                          Name
                                        </th>
                                        <th scope="col" class="text-sm font-medium text-gray-900 px-4 py-3 text-left">
                                          Email
                                        </th>
                                        <th scope="col" class="text-sm font-medium text-gray-900 px-4 py-3 text-left">
                                          Password
                                        </th>
                                        <th scope="col" class="text-sm font-medium text-gray-900 px-4 py-3 text-left">
                                          Dob
                                        </th>
                                        <th scope="col" class="text-sm font-medium text-gray-900 px-4 py-3 text-left">
                                          Accepted terms?
                                        </th>
                                      </tr>
                                    </thead>
                                    <tbody id="table_tbody">
                                    </tbody>
                                  </table>
                                </div>
                              </div>
                            </div>
                          </div>


                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
</body>
</html>
