<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<h1>Node_MCU-to-Thingboards</h1>

<h2>Description</h2>
<p>Node_MCU-to-Thingboards is a project designed to collect data from various sensors and components using a NodeMCU and transfer this data to ThingsBoard, an open-source IoT platform. This project provides a comprehensive guide for setting up the NodeMCU, configuring the sensors, and sending the collected data to the ThingsBoard server.</p>

<h2>Table of Contents</h2>
<ul>
    <li><a href="#description">Description</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#features">Features</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#authors-and-acknowledgements">Authors and Acknowledgements</a></li>
    <li><a href="#contact-information">Contact Information</a></li>
    <li><a href="#additional-sections">Additional Sections</a></li>
</ul>

<h2 id="installation">Installation</h2>

<h3>Prerequisites</h3>
<ul>
    <li><a href="https://en.wikipedia.org/wiki/NodeMCU" target="_blank">NodeMCU</a></li>
    <li>Sensors (e.g., temperature sensor, humidity sensor, etc.)</li>
    <li><a href="https://www.arduino.cc/en/software" target="_blank">Arduino IDE</a></li>
    <li><a href="https://thingsboard.io/" target="_blank">ThingsBoard account</a></li>
</ul>

<h3>Steps</h3>
<ol>
    <li>
        <strong>Setup the Arduino IDE:</strong>
        <ul>
            <li>Install the Arduino IDE from the <a href="https://www.arduino.cc/en/software" target="_blank">official website</a>.</li>
            <li>Add the NodeMCU board to the Arduino IDE. Follow the guide <a href="https://randomnerdtutorials.com/installing-the-esp8266-board-in-arduino-ide-windows-instructions/" target="_blank">here</a>.</li>
        </ul>
    </li>
    <li>
        <strong>Install Required Libraries:</strong>
        <ul>
            <li>Open the Arduino IDE and go to <code>Sketch -> Include Library -> Manage Libraries</code>.</li>
            <li>Install the following libraries:
                <ul>
                    <li><code>ESP8266WiFi</code></li>
                    <li><code>PubSubClient</code></li>
                </ul>
            </li>
        </ul>
    </li>
    <li>
        <strong>Clone the Repository:</strong>
        <ul>
            <li>Clone this repository to your local machine using:
                <pre><code>git clone https://github.com/ZeroN257/Node_MCU-to-Thingboards.git</code></pre>
            </li>
        </ul>
    </li>
    <li>
        <strong>Configure the Code:</strong>
        <ul>
            <li>Open the <code>Node_MCU-to-Thingboards.ino</code> file in the Arduino IDE.</li>
            <li>Update the WiFi credentials:
                <pre><code>const char* ssid = "your_SSID";<br>const char* password = "your_PASSWORD";</code></pre>
            </li>
            <li>Update the ThingsBoard server and access token:
                <pre><code>const char* thingsboardServer = "your_thingsboard_server";<br>const char* accessToken = "your_access_token";</code></pre>
            </li>
        </ul>
    </li>
    <li>
        <strong>Upload the Code:</strong>
        <ul>
            <li>Connect your NodeMCU to your computer.</li>
            <li>Select the correct board and port from <code>Tools -> Board</code> and <code>Tools -> Port</code>.</li>
            <li>Click on the Upload button to upload the code to the NodeMCU.</li>
        </ul>
    </li>
</ol>

<h2 id="usage">Usage</h2>
<ol>
    <li><strong>Connect Sensors:</strong>
        <ul>
            <li>Connect your sensors to the NodeMCU according to the sensor specifications and the pins defined in the code.</li>
        </ul>
    </li>
    <li><strong>Power Up the NodeMCU:</strong>
        <ul>
            <li>Once powered, the NodeMCU will connect to the specified WiFi network and start collecting sensor data.</li>
        </ul>
    </li>
    <li><strong>View Data on ThingsBoard:</strong>
        <ul>
            <li>Log in to your ThingsBoard account.</li>
            <li>Navigate to the device configured with the NodeMCU's access token.</li>
            <li>Visualize the incoming data on the ThingsBoard dashboards.</li>
        </ul>
    </li>
</ol>

<h2 id="features">Features</h2>
<ul>
    <li>Easy integration of various sensors with NodeMCU.</li>
    <li>Real-time data transfer to ThingsBoard.</li>
    <li>Configurable via Arduino IDE.</li>
    <li>Extensible to support additional sensors and components.</li>
</ul>

<h2 id="contributing">Contributing</h2>
<p>We welcome contributions! Please follow these steps:</p>
<ol>
    <li>Fork the repository.</li>
    <li>Create a new branch (<code>git checkout -b feature/your-feature-name</code>).</li>
    <li>Commit your changes (<code>git commit -am 'Add some feature'</code>).</li>
    <li>Push to the branch (<code>git push origin feature/your-feature-name</code>).</li>
    <li>Create a new Pull Request.</li>
</ol>

<h2 id="license">License</h2>
<p>This project is licensed under the MIT License - see the <a href="LICENSE">LICENSE</a> file for details.</p>

<h2 id="authors-and-acknowledgements">Authors and Acknowledgements</h2>
<ul>
    <li><strong>Nguyen Duc Le Nguyen</strong> - Initial work - <a href="https://github.com/ZeroN257" target="_blank">ZeroN257</a></li>
</ul>


<h2 id="contact-information">Contact Information</h2>
<p>For any questions or support, please open an issue in the repository or contact me at <a href="mailto:your.email@example.com">your.email@example.com</a>.</p>

<h2 id="additional-sections">Additional Sections</h2>

<h3>FAQs</h3>
<p><strong>Q:</strong> How can I add more sensors?<br>
<strong>A:</strong> You can add more sensors by connecting them to available pins on the NodeMCU and updating the code to read from these sensors.</p>

<p><strong>Q:</strong> What if my NodeMCU doesn't connect to WiFi?<br>
<strong>A:</strong> Ensure that you have entered the correct SSID and password. Also, make sure your router is within range.</p>

<h3>Troubleshooting</h3>
<ul>
    <li><strong>NodeMCU not recognized by Arduino IDE:</strong> Ensure you have installed the correct drivers for the NodeMCU.</li>
    <li><strong>Data not showing on ThingsBoard:</strong> Verify that the access token and server address are correct in the code.</li>
</ul>

</body>
</html>
