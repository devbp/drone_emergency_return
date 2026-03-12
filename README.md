# drone_emergency_return
This project implements an automated Software‑in‑the‑Loop (SIL) test for validating a drone’s Emergency Return‑to‑Home (RTH) behavior when the battery level drops below a critical threshold.

The test is fully automated using pytest, supports CSV‑based parametrization, and includes robust precondition checks, mission simulation, battery drain simulation, and final landing verification.

Running the Tests
1. Install dependencies
   
    pip install -r requirements.txt
   
3. Run all tests

pytest -v


The main test case implemented is:

TC‑E‑005‑EXT — Emergency Return on Critical Battery

How the Test Works
1. Parametrized Inputs
The test loads battery and wind values from:

test_data/test_data.csv

Each row becomes one test execution.

Test Case Description
Purpose
Validate that the drone:

Powers on and initializes correctly

Meets all preconditions (battery, wind, GPS, HOME position)

Starts a mission and flies to a waypoint

Detects critical battery level

Automatically switches to RTH mode

Returns to HOME

Lands successfully
