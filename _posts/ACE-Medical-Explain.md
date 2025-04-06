# ACE Medical
  ## AI
  ### Medic AI
  Allow AI to heal injured soldiers
  
  ### Require Items
  AI will only heal when have items, like bandages
  
  ## Blood
  ### Enable Blood Drops
  Blood texture spawned on the ground when bleeding
  
  ### Max Blood Objects
  Max Blood texture amount
  
  ### Blood Lifetime
  Blood texture lifetime


  ## States
  ### Player Fatal Injuries
  When the injury on player could be ***fatal***  
  ***fatal*** means injury that could cause death  
  **Always**: Always  
  **In Cardiac Arrest**: Only in Cardiac Arrest, which means only when unconscious and Cardiac Arrest  
  **Never**: Never, which means a shot to player will never cause directly death  
  
  ### AI Fatal Injuries
  SAME AS Player
  
  ### AI Unconsciouness
  Disable: when AI enter unconscious, the ai will automatically go dead  
  
  ### Cardiac Arrest Time
  Countdown time after enter Cardiac before death
  
  ### Bleedout During Cardiac Arrest
  When disabled, the unit will not die after lose all his blood During Cardiac Arrest
  

  ## Status
  ### Bleeding Coefficient
  higher means faster bleeding on same wound
  
  ### Pain Coefficient
  higher means more pain on same wound
  
  ### IV Transfusion Flow Rate
  1.0=250ml/min  
  higher means quicker
  

  ## Vitals
  ### Enable SpO2 Simulation
  well, idk yet



# ACE Medical Interface
  ## Feedback
  ### Pain Effect Type
  ```sqf
  [player, 1] call ace_medical_fnc_adjustPainLevel
  ```
  <details>
    <summary>White Flashing</summary>
    <img src="https://github.com/user-attachments/assets/5fb59c09-570c-4708-bae8-7942f1a57467">
  </details>
  
  <details>
    <summary>Pusling Blur</summary>
    <img src="https://github.com/user-attachments/assets/2ffa7916-7da1-4050-8370-8ab591777aee">
  </details>

  <details>
    <summary>Chromatic Aberration</summary>
    <img src="https://github.com/user-attachments/assets/009adf25-749d-44bb-b2b4-93e77421afd5">
  </details>

  <details>
    <summary>Only high pain effect</summary>
    same as Pusling Blur?
  </details>

  ### Low Blood Volume Effect Type
  ### Enable Fracture/Tourniquet/Splint Indicators

  ## GUI
  ### Enable Medical Actions
  ### Enable Medical Self Actions
  ### Enable Medical Menu
  ### Reopen Medical Menu
  ### Maximum Distance
