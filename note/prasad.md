# Current Time in India (IST)

To see the live time in India (IST), open the following HTML file in your browser.

## Instructions:

1. Copy the following HTML code into a file called `index.html`:

   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <style>
           body { 
               width: 35em; 
               margin: 0 auto; 
               font-family: Tahoma, Verdana, Arial, sans-serif; 
               text-align: center; 
           }
       </style>
   </head>
   <body>
       <h1>Current Time in India (IST)</h1>
       <p>Time: <span id="datetime"></span></p>

       <script>
           function getIndiaTime() {
               // Get current time in IST
               var indiaTime = new Date().toLocaleString("en-US", { timeZone: "Asia/Kolkata" });
               document.getElementById("datetime").innerHTML = indiaTime;
           }

           // Update time every second
           setInterval(getIndiaTime, 1000);
           getIndiaTime();  // Set the initial time immediately
       </script>

   </body>
   </html>
