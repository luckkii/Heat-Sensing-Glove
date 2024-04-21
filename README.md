<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ScorchSafe Readme
</head>
<body>
  <h1>ScorchSafe - Temperature Sensing Glove</h1>

  <h2>Purpose</h2>
  <p>The program takes in an input from the temperature sensors which is then converted into volts and then degrees in Celsius. This value is then used to check whether the temperature is above a certain threshold, which is 53 degrees Celsius in our case. If the temperature crosses this threshold, then the buzzer makes a noise, however, if the temperature is below, it stays silent.
</p>

  <h2>Components</h2>
  <ul>
    <li>Battery: Provides power to the system.</li>
    <li>Temperature Sensors:
      <ul>
        <li>Index Finger Sensor: Connected to analog pin A0.</li>
        <li>Thumb Finger Sensor: Connected to analog pin A2.</li>
        <li>Palm 1 Sensor: Connected to analog pin A3.</li>
        <li>Palm 2 Sensor: Connected to analog pin A5.</li>
      </ul>
    </li>
    <li>Buzzer: Used for providing audible alerts. Connected to pin 7 for power.</li>
  </ul>

  <h2>Setup</h2>
  <p>Make sure the components are connected as described above and in our documentation before uploading the code to your microcontroller board (e.g., LilyPad Arduino).</p>

  <h2>Code Overview</h2>
  <ul>
    <li>Variables:
      <ul>
        <li><code>buzzer_vcc</code>: Pin number for the buzzer VCC connection.</li>
        <li><code>temp_sens</code>, <code>temp_sens_2</code>, <code>temp_sens_3</code>, <code>temp_sens_4</code>: Analog pins connected to the temperature sensors.</li>
        <li><code>time</code>: Delay time between temperature readings and buzzer alerts.</li>
      </ul>
    </li>
    <li>Constants:
      <ul>
        <li><code>C</code>, <code>D</code>: Constants representing specific tones for the buzzer.</li>
      </ul>
    </li>
    <li>Loop:
      <ul>
        <li>Reads temperature values from each sensor and converts them to Celsius.</li>
        <li>Prints temperature values to the serial monitor.</li>
        <li>If any temperature reading exceeds the predefined maximum (33 degrees Celsius), it activates the buzzer. Otherwise, the buzzer won't buzz.</li>
      </ul>
    </li>
  </ul>

  <h2>Additional Information</h2>
  <ul>
    <li>The temperature values read from the sensors are converted from analog readings to volts and then to degrees (Celsius).</li>
    <li>The threshold for activating the buzzer is set at 33 degrees Celsius. If any sensor detects a temperature above this threshold, the buzzer will sound.</li>
    <li>The buzzer remains silent if the temperature readings are below the threshold.</li>
  </ul>
</body>
</html>
