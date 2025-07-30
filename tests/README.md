# Test Suite for Autarky Models

This folder contains test scripts to verify that each optimization model in the repository:
- Runs without errors
- Produces expected result files (e.g., CSV, JSON)

## Default Case Studies

Each model (Deterministic, Expected, ICC, JCC) is tested using the pre-loaded inputs inside their respective `/inputs` folder.

The inputs are minimal exemplative test cases intended to:
- Validate functionality
- Keep runtime low for the sake of quick testing

---

### Deterministic Model

#### **Overview**

The deterministic test model simulates a **remote island community in Kenya**, where energy needs span both residential and productive uses. The modeled users include:

- Households with basic electricity needs (lighting, phone charging)
- Micro-enterprises using power tools, refrigeration, and milling machines
- Public services such as health centers and schools

The load demand profile has been simulated using the [RAMP tool](https://github.com/energy-modelling-toolkit/ramp), which generates representative profiles based on local energy use patterns and activity-based modeling.
Key demand characteristics are: Average daily peak power of ~30 kW and Average daily energy use of 486 kWh.

#### **Load Profile Visualization**

![Load Profile Overview](https://github.com/AleOnori98/Autarky-2.0/blob/main/tests/images/load_profile.png)

> *Figure: Hourly demand profile for a typical day in wet and dry seasons.*

---

#### **System Configuration**

The system is designed as a fully off-grid hybrid mini-grid with the following specifications:

- **Project lifetime**: 20 years (used for long-term cost minimization and net present cost calculation)
- **Dispatch resolution**: Hourly (daily operation)
- **Seasons modeled**: Wet and dry
- **Minimum renewable energy share**: 70%
- **Grid connection**: None (fully off-grid)
- **Lost load allowed**: ❌ No (full demand satisfaction required)

##### **Technologies included:**

- **Solar PV** (with seasonal availability from [Renewables.ninja](https://www.renewables.ninja/))
- **Battery storage** (including round-trip efficiency, state of charge limits, and degradation)
- **Diesel generator** (with partial load efficiency curve)

![System Layout](https://github.com/AleOnori98/Autarky-2.0/blob/main/tests/images/system_layout.png)

> *Figure: System schematic showing solar PV, battery, and diesel backup configuration.*

#### **Results:**

The optimal system configuration for the Kenyan island community includes an 88.7 kW solar PV array, 125.5 kWh of battery storage, and a 15.4 kW diesel generator. The model achieves a 70% renewable penetration with no lost load, meeting all demand reliably. The total Net Present Cost of the project is approximately 157 kUSD, with a Total Investment Cost 117.68 kUSD resulting in a quite high levelized cost of energy (LCOE) of 0.57 USD/kWh. Annual Solar Curtailment Share is 9.62 % of total solar production while Annual fuel consumption is around 5,078 tons of liters per year, with the generator operating at an average efficiency of 10.5 kWh/liter and a load factor of nearly 40%.

---


