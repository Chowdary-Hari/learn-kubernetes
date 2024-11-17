# Current Time in India (IST)

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
