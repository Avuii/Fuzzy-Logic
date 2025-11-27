# 🤖 Fuzzy-Logic

Two fuzzy-logic control systems written in FCL and executed using jFuzzyLogic.
  
--- 
  
## 🧠 What Is Fuzzy Logic?  
  
Fuzzy logic is a mathematical approach used to model human-like reasoning in situations where data is imprecise, vague, or continuous.  
Instead of strict binary values like:  
* distance = near or far  
* speed = low or high
  
…fuzzy logic allows intermediate states, such as:

* a bit near  
* somewhat fast
  
This makes it ideal for real-world systems like braking control, washing machines, air-conditioning, or autonomous vehicles.  
  
---
  
## 🔄 How a Fuzzy System Works
  
* **Fuzzification** – crisp inputs → fuzzy sets  
* **Inference** – apply IF/THEN rules  
* **Defuzzification** – fuzzy output → final numeric value  
Both simulations in this repo follow this exact method.  

---
  
## 🧩 Project Structure
  
```bash
/Fuzzy-Logic  
│  
├── Breaking-symulation/   
│   ├── breaking.fcl                    # Fuzzy braking model  
│   └── Breaking-symulation.pdf         # Documentation & charts  
│  
├── Washing-machine-symulation/  
│   ├── wm-symulation.fcl               # Washing machine fuzzy model  
│   └── wm-symulation.pdf               # Analysis & results  
│  
├── jFuzzyLogic.jar                      # Library for running FCL files  
├── LICENSE  
└── README.md  
```
---
  
## 🚗 Vehicle Braking Simulation  
  
A fuzzy controller determining braking intensity based on:
* **distance to obstacle**
* **vehicle speed**
  
Output:
braking_force
  
##### 📝 [Project](./Breaking-symulation/breaking.fcl)
##### 📄 [Detailed Report](./Breaking-symulation/Breaking-symulation.pdf)
  

## Washing Machine Simulation
  
A fuzzy controller that selects wash time based on:
* **dirtiness level**
* **dirt type**
  
Output:
wash_time 
  
#### 📝 [Project](./Washing-machine-symulation/wm-symulation.fcl)
#### 📄 [Detailed Report](./Washing-machine-symulation/wm-symulation.pdf)
  
---
  
## 📦 Technologies
  
FCL (Fuzzy Control Language)  
Java 8+  
jFuzzyLogic.jar (included)  
  
---
  
## 🚀 How to Run the FCL Files  
  
1️⃣ Check Java installation  
`java -version`  
  
2️⃣ Run any FCL model using jFuzzyLogic  
`java -jar jFuzzyLogic.jar -e <file.fcl> <input1> <input2>`  
  
---
  
#### ▶️ Example: Vehicle Braking Simulation  
`java -jar jFuzzyLogic.jar -e Breaking-symulation/breaking.fcl 500 50`  
  
Inputs:  
500 → distance
50 → speed  
  
#### ▶️ Example: Washing Machine Simulation  
`java -jar jFuzzyLogic.jar -e Washing-machine-symulation/wm-symulation.fcl 70 20`  
  
Inputs:
70 → dirtiness  
20 → dirt type  

    
---

  
# 🧑‍💻 Author

Created for educational purposes by Avui.
