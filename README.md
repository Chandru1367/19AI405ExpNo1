<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: CHANDRU M</h3>
<h3>Register Number: 212224230041</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Weather Monitoring Agent:</h3>
<p>
A Weather Monitoring Agent continuously monitors weather conditions in a city by collecting
environmental data such as temperature, rainfall, and wind speed. Based on the weather
conditions, the agent issues appropriate alerts such as a <b>Heatwave Alert</b>,
<b>Flood Warning</b>, or <b>Storm Warning</b>. If all weather parameters are within the
safe range, the agent reports that the weather is normal. The environment considered here
is a city where weather conditions are generated randomly. The agent keeps monitoring the
weather until normal conditions are observed.
</p>

<hr>

<h3>PEAS DESCRIPTION:</h3>
<table border="1" cellpadding="5" cellspacing="0">
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
    <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
  <tr>
    <td><strong>Weather Monitoring Agent</strong></td>
    <td><strong>Accurate weather monitoring and timely weather alerts</strong></td>
    <td><strong>City, Weather Conditions</strong></td>
    <td><strong>Weather Alerts (Heatwave, Flood, Storm)</strong></td>
    <td><strong>Temperature, Rainfall, Wind Speed</strong></td>
  </tr>
</table>

<hr>

<h3>DESIGN STEPS</h3>

<h3>STEP 1: Identifying the Input:</h3>
<p>
Temperature, rainfall, and wind speed collected from the weather sensors.
</p>

<h3>STEP 2: Identifying the Output:</h3>
<p>
Issue a Heatwave Alert if the temperature is greater than 40°C, a Flood Warning if
rainfall is greater than 50 mm, a Storm Warning if wind speed is greater than 80 km/h;
otherwise display "Weather is normal."
</p>

<h3>STEP 3: Developing the PEAS Description:</h3>
<p>
The PEAS description is developed by identifying the Performance, Environment,
Actuators, and Sensors of the Weather Monitoring Agent.
</p>

<h3>STEP 4: Implementing the AI Agent:</h3>
<p>
Monitor weather conditions continuously, analyze the sensed data, and issue the
appropriate weather alert whenever abnormal conditions are detected.
</p>

<h3>STEP 5:</h3>
<p>
Measure the performance parameters: The agent's performance is evaluated based on
accurate monitoring and timely weather alerts. The monitoring process continues until
the weather conditions become normal.
</p>

<h3>PYTHON PROGRAM</h3>

```python

import random

class WeatherAgent:
    def __init__(self, city):
        self.city = city

    def monitor_weather(self):
        while True:
            state = self.sensors.get_weather_state()
            action = self.choose_action(state)
            self.actuators.perform_action(action)

            if action == "Weather is normal":
                break

    def choose_action(self, state):
        if state["temperature"] > 40:
            return "Issue heatwave alert"
        elif state["rainfall"] > 50:
            return "Issue flood warning"
        elif state["wind_speed"] > 80:
            return "Issue storm warning"
        else:
            return "Weather is normal"


class WeatherSensors:
    def get_weather_state(self):
        return {
            "temperature": random.randint(20, 45),
            "rainfall": random.randint(0, 100),
            "wind_speed": random.randint(10, 100)
        }


class WeatherActuators:
    def perform_action(self, action):
        print(action)


sensor = WeatherSensors()
actuator = WeatherActuators()

agent = WeatherAgent("Chennai")
agent.sensors = sensor
agent.actuators = actuator

agent.monitor_weather()

```
<h3>OUTPUT</h3>

<img width="884" height="141" alt="image" src="https://github.com/user-attachments/assets/e13e30d5-a183-4c5a-b2dd-da8a58d08883" />

<h3>RESULT</h3>

<p>The result of the Weather Monitoring Agent experiment is that the AI agent successfully monitored the weather conditions of the city by checking the temperature, rainfall, and wind speed. Based on the sensed values, the agent correctly issued a Heatwave Alert, Flood Warning, or Storm Warning whenever the weather conditions exceeded the specified thresholds. The agent continued monitoring until all weather parameters returned to normal, after which it displayed "Weather is normal" and terminated the monitoring process.</p>


