
![Screenshot 2025-04-02 072220](https://github.com/user-attachments/assets/b792d2fe-4899-4269-b525-f5440b2fd3f0)


# Overview # 
The Packaging Fundamentals of Design and Technology Workshop bridges the gap between traditional chip design and modern packaging.<br>
It gives a solid understanding of advanced packaging techniques.<br>
The workshop helps in making better decisions for system-level integration.<br>
Participants explore the evolution of packaging and interconnect technologies.<br>
It also covers thermal simulations, assembly processes, and packaging selection.<br>
Hands-on activities offer practical insights throughout the course.<br>


# Index #

## [Module 1] ## 
  
### Packaging Evolution: From Basics to 3D Integration ###

-  L1 : Introduction To Semiconductor Packaging And Industry Overview
-  L2 : Understanding Package Requirements And Foundational Package Types
-  L3 : Evolving Package Architectures - From Single Chip To Multi-Chip Modules
-  L4 : Interposers Re-distribution Layers And 2.5D/3D Packaging Approaches
-  L5 : Comparative Analysis And Selecting The Right Packaging Solution

## [Module 2] ## 

### From Wafer to Package: Assembly and Manufacturing Essentials ###

- L1 : Setting The Stage - Supply Chain And Facilities
- L2 : Wafer Pre-Preparation - Grinding And Dicing
- L3 : Wire Bond Packaging - Die Attach To Molding
- L4 : Flip Chip Assembly - Bump Formation And Underfill
- L5 : Wafer Level Packaging And Conclusion

## [Module 3] ## 

### Labs: Thermal Simulation of Semiconductor Packages with ANSYS ###

- L1 : Introduction And Getting Started With ANSYS Electronics Desktop
- L2 : Setting Up A Flip-Chip BGA Package
- L3 : Material Definitions And Thermal Power Sources
- L4 : Meshing And Running The Thermal Analysis
- L5 : Viewing Results And Exploring Other Package Types

## [Module 4] ## 

### Ensuring Package Reliability: Testing and Performance Validation ###

- L1 : Introduction to Package Testing and Electrical Functionality Checks
- L2 : Reliability and Performance Testing of Semiconductor Packages

## [Module 5] ##  

### Package Design and Modeling: Building a Semiconductor Package from Scratch ### 

- L1 : Introduction to Package Cross-Section Modeling in ANSYS Electronics Desktop (AEDT)
- L2 : Creating the Die and Substrate in AEDT 
- L3 : Adding Die Attach Material and Bond Pads 
- L4 : Wire Bond Creation and Material Assignment 
- L5 : Applying Mold Compound and Finalizing the Package Model 

--------------------------------------------------------------------------------------------
# Content #
--------------------------------------------------------------------------------------------

##  [Module 1] ##

###  Introduction To Semiconductor Packaging And Industry Overview ###

- How does IC package looks like ? What info in present on package ?
  
  On top of a semiconductor IC (Integrated Circuit) package, you'll typically find the following information:
  
  **[1] Manufacturer's Logo/Name:** Indicates the company that produced the IC<br>
  **[2] Part Number:** Unique identifier for the IC, specifying its type and specifications.<br>
  **[3] Date Code:** Represents the manufacturing date, often in a format like week/year or year/month.<br>
  **[4] Lot Number:** Used for tracking batches of production for quality control.<br>
  
  Below fig shows on example of package IC
  
  ![M1_L1p1](https://github.com/user-attachments/assets/cbffc88f-9880-42a9-bab2-2e6698dcdca3)

- Why semiconductor packaging required?

  **[1] Protection:** Safeguards the fragile die from physical damage, moisture, and corrosion<br>
  **[2] Electrical Connections:** Provides necessary pins or leads for connecting the chip to external circuits<br>
                             
  ![M1_L1p2](https://github.com/user-attachments/assets/1458d929-7dbe-4310-aec3-210c7e19666f)

- Following are the different parts of package
  
  ![M1_L1p5](https://github.com/user-attachments/assets/b1610b9e-e420-4b8b-83ef-897a283c6ad1)

- Key Players in the Semiconductor Industry
  
  **[1] Fabless:**  Companies that design semiconductors but outsource manufacturing to foundries (e.g., Qualcomm, NVIDIA).<br>
  **[2] Foundry:** Companies that specialize in semiconductor fabrication, producing chips designed by fabless companies (e.g., TSMC, Samsung).<br>
  **[3] OSAT (Outsourced Semiconductor Assembly and Test):** Companies that handle the packaging, assembly, and testing of semiconductors after fabrication (e.g., ASE, Amkor)<br>

  ![M1_L1p6](https://github.com/user-attachments/assets/6b5a24ef-0241-44c5-ab16-0f8a17d2ff17)

### Understanding Package Requirements And Foundational Package Types ###

- Factors to Consider When Choosing the Right Package for Your Die
  
  **[1] Pin Count:** No. of I/O , High-speed I/O requirements can influence the package selection<br>
  **[2] Thermal Dissipation :** Organic packages are not suitable for temperatures over 200°C; ceramic packages are used in such cases for better heat dissipation<br>
  **[3] Cost:** depends on budget constraints<br>
  **[4] Form Factor (Area):** The physical space available for the package on the board can limit the type of package used<br>

  The package serves to connect the chip to the board, impacting both performance and durability of the final product
  
  ![M1_L2p3](https://github.com/user-attachments/assets/5fe8c6c2-c993-4b9a-8419-dfc7c81b4430)

- Overview of Package Structure
  
  **[1] Typical Package Structure :** Includes the die, carrier, mold compound, and system board (PCB), all connected through interconnects.<br>
  **[2] Carrier Materials :** Carriers can be made from materials like leadframe, laminate, plastic, ceramic, or silicon.<br>
  **[3] Interconnection Methods :** Includes wirebond and bump/solder.<br>
  **[4] Package Types :** Come in various types, such as Dual In package (DIP) , Quad flat no leads (QFN) , chip scale package (CSP), package on package (PoP), and advanced ones like Intel’s MCM(multichip package) and Nvidia’s CoWoS.<br>
  
  ![M1_L2p4](https://github.com/user-attachments/assets/6c7f181b-dfea-4b04-ab06-2b2196a6a31d)

### Evolving Package Architectures - From Single Chip To Multi-Chip Modules ###

- Anatomy of packages
  
  **[1] Package Anatomy** – Includes different substrate types like leadframe, laminate, and advanced package substrates.<br>
  **[2] Leadframe-based Packages** – Examples include DIP, QFN; they use gold wirebonds and are simpler in design.<br>
  **[3] Laminate-based Packages** – Examples include PBGA, FC-CSP; they offer higher pin density and provide better performance.<br>
  **[4] Advanced Packages** – Examples include 2.5D CoWoS; they integrate multiple dies using interposers for high bandwidth and compact size<br>

  ![M1_L3p2](https://github.com/user-attachments/assets/dc9ddced-97f5-47e7-a336-01e18feffa30)

### Interposers Re-distribution Layers And 2.5D/3D Packaging Approaches ###

- following the different approches for packaging<br>
  **[1] DIP** – Dual In-line Package<br>
  **[2] SIP** – Single In-line Package<br>
  **[3] PGA** – Pin Grid Array (In DIP, pins need space, but in PGA, the pins are arranged underneath the package to save space.)<br>
  **[4] QFN** – Quad Flat No-lead (The package is flat with no leads coming out, with leads on all four sides.)<br>
  **[5] QFP** – Quad Flat Package (Leads are coming out from all four sides of the package.)<br>
  **[6] PBGA** – Plastic Ball Grid Array (The die is connected from the other side of the package using balls as connections.)<br>
  **[7] LGA** – Land Grid Array (No leads or pins come out; the contacts are flat, directly placed on the board.)<br>
  **[8] CSP** – Chip-Size Package (The package size is similar to the chip size.)<br>
            It is used when there is limited space on the board, so the chip directly contacts the board without extra space for leads & also referred to as Chip-Scale Package.<br>
  **[9] MCM** – Multi-Chip Module (A package that contains multiple chips inside.)<br>
  **[10] PoP** – Package-on-Package (Two packages stacked on top of each other, such as PBGA on PBGA.)<br>
  **[11] COB** – Chip-on-Board (The die is directly mounted on the board without any package, and connections are made using wire bonds or flip-chip bonding.)<br>

  ![M1_L4p1](https://github.com/user-attachments/assets/2d3c92be-e8f8-4410-9378-abc7c273bc21)

### Comparative Analysis And Selecting The Right Packaging Solution ###

- Based on the specific requirements and a thorough evaluation of the pros and cons, we can confidently select the most suitable package option as mention in below table
  For example, if form factor is a concern, the FC-CSP type of package is a good choice. On the other hand, if high performance with lower cost and power consumption is the priority, moving to an advanced package would be the best option

  ![M1_L5p1](https://github.com/user-attachments/assets/ba70b644-dd7c-4044-8ed9-bc0fc80e27e8)


##  [Module 2] ##

### Setting The Stage - Supply Chain And Facilities ###

This figure outlines the semiconductor supply chain process.<br>
- It starts with IC design at the design house using EDA tools and PDKs to create the circuit blueprint.<br>
- The next step is wafer fabrication, where silicon wafers and materials are used to manufacture the chips.<br>
- After fabrication, the chips undergo package assembly and testing, ensuring each IC is properly enclosed and functional.<br>
- The packaged ICs are then integrated onto PCBs during board assembly and testing.<br>
- Finally, in the product assembly and test phase, all components are assembled into the final product and undergo comprehensive testing before release<br>

  ![M2_L1p1](https://github.com/user-attachments/assets/cc8645c8-b20f-442e-9600-99bd8d425d41)

### Wafer Pre-Preparation - Grinding And Dicing ### 

- ATMP unit<br>
  The ATMP unit for VLSI chips is divided into three main areas: 60% of the space is a clean room for assembly, ensuring contamination-free processing of chips;<br?
  30% is dedicated to testing, where the chips undergo functional and quality checks; and 10% is used for materials storage, holding components like substrates, bonding wires, and packaging materials<br>

![M2_L1p2](https://github.com/user-attachments/assets/db70d5d1-1128-417b-84fc-90a0f94ba823)

- following is the initial stages of wafer handling and preparation
  - ISO 7 : A cleanroom classification by ISO, allowing no more than 352,000 particles per cubic meter (0.5 microns or larger).<br>
        ISO 7 cleanrooms are used in processes like wafer fabrication, where controlling contamination is crucial for product quality.<br>
  - Carrier : Used to transport the wafer; can be either vertical or horizontal.<br>
  - 12-inch Wafer : With a thickness of 800 microns, this results in a larger package size.<br>
                    The actual circuit is on the top, while the underside is just the substrate. The goal is to reduce the substrate area.<br>
  - Wafer Inspection : Performed to ensure the wafer meets quality standards before further processing.<br>
  - Lamination : The front side of the wafer is laminated, where the circuit is located.<br>
  - Grinding : The back side of the wafer is ground in a machine (after flipping the wafer).<br>
               This step subjects the wafer to stress, which can cause breakage.<br>
  - Frame Attachment : A frame is applied to the back side of the wafer using tape for support.<br>
  - Wafer Dicing : The wafer is diced using either a laser or a blade to separate individual chips.<br>

  ![M2_L2p1](https://github.com/user-attachments/assets/21fe6fa3-d090-4f71-a9a1-f3dc14565f89)

### Wire Bond Packaging - Die Attach To Molding ###

- Following is the step by step process for wire bond packaging :-<br>

  **[1] Die Attach** (Epoxy Dispensing & Placement) - Epoxy is dispensed in a defined pattern on the substrate or DAF. The chip is picked and accurately placed on the epoxy-coated area.<br>
  **[2] Curing** - The assembly is heated to harden the epoxy and secure the die in place.<br>
  **[3] Wire Bonding** - Fine gold or aluminum wires connect die pads to package leads.<br>
                       - Ball bond is formed on the die pad using heat and pressure.<br>
                       - Wire is looped to reach the corresponding substrate pad.<br>
                       - Crescent bond is made on the substrate pad with ultrasonic energy.<br>
  **[4] Molding (Encapsulation)** - Liquid resin is injected to cover and protect the die and wires. Molding ensures mechanical support and environmental sealing.<br>
  **[5] Marking** - Laser is used to engrave part numbers or batch IDs on the package.<br>
  **[6] Dicing** - A precision blade cuts the molded wafer into individual IC packages.<br>
   
 ![M2_L3p6](https://github.com/user-attachments/assets/0f756773-012d-4b27-a85b-5704be679c79)

- Following is the detail process of wire bonding done 

![M2_L3p3](https://github.com/user-attachments/assets/ba8c89d7-752a-4562-a2e4-cdb971d47a86)

### Flip Chip Assembly - Bump Formation And Underfill ###

  **[1] Bump Formation** - Solder bumps are formed at the die’s fan-out points for connection.<br>
  **[2] Chip Flipping** - The die is flipped so that the solder bumps face the package substrate.<br>
  **[3] Flux Dispensing** - Flux is applied to bond pads to improve solder adhesion and prevent oxidation.<br>
  **[4] Chip Placement** - The flipped die is aligned and placed onto the substrate, with bumps sitting on the pads.<br>
  **[5] Solder Reflow** - The assembly is heated, melting the solder bumps to form electrical and mechanical bonds.<br>
  **[6] Flux Cleaning** - Any residual flux is removed using a solvent spray to prevent defects.<br>
  **[7] Underfill Dispensing** - Underfill epoxy is injected to fill gaps and reduce stress from different thermal expansion rates.<br>
  **[8] Underfill Curing** - The underfill is cured using heat to strengthen the die-to-substrate connection.<br>
  **[9] Molding** - A protective mold compound is applied to shield the package from environmental damage.<br>
  **[10] Marking** - A laser is used to engrave product information, batch numbers, or identification codes.<br>
     
  ![M2_L4p2](https://github.com/user-attachments/assets/ff5d3a7c-ba2e-4dcf-a5b2-703b51829e78)

###  Wafer Level Packaging And Conclusion ###

  Reconstitution – Known good dies are embedded in a reconstituted wafer using an epoxy mold compound to allow uniform wafer-level processing and easy handling.<br>
  RDL (Redistribution Layer) Preparation – The RDL is applied to extend and reroute the die’s I/O connections, enabling proper alignment with solder bumps for packaging.<br>

  ![M2_L5p1](https://github.com/user-attachments/assets/14e77b9a-0b12-42c9-91c2-1cc205e13a0c)


## [Module 3] ## 

### Introduction And Getting Started With ANSYS Electronics Desktop ###

- Understand the options availabe in ANSYS Desktop :- 

![M3_L1p1](https://github.com/user-attachments/assets/6c0b6ff7-5496-4964-88ee-74dcbc6cb47f)
![M3_L1p2png](https://github.com/user-attachments/assets/5e3532fa-992a-41fc-b30c-350ea72e4950)

- Loading the available package available in tool for thermal analysis purpose :- 

![M3_L1p3](https://github.com/user-attachments/assets/1ae1f1a2-03c9-4855-9ecb-65e1fab834f9)

### Setting Up A Flip-Chip BGA Package ###

- Review the dimension & material used for the package :- 

![M3_L2p1](https://github.com/user-attachments/assets/ee9c9d51-deb7-4ea4-91c9-1b921000155f)
![M3_L2p2](https://github.com/user-attachments/assets/bfb169b4-e533-477d-8b10-702b21f9c08d)
![M3_L2p3](https://github.com/user-attachments/assets/7da9bf18-d9aa-45dd-b9ed-38484f971047)
![M3_L2p4](https://github.com/user-attachments/assets/8d5cf820-8404-4419-9fd0-4a6e6c8f1588)
![M3_L2p5](https://github.com/user-attachments/assets/fcacf57d-2761-455c-9819-b8654e8a34c7)
![M3_L2p6](https://github.com/user-attachments/assets/17d6a348-21fa-4499-8cf7-bb88be31dd40)
![M3_L2p7](https://github.com/user-attachments/assets/ce6fc36c-ad46-4dee-9484-9a582f115db2)
![M3_L2p8](https://github.com/user-attachments/assets/057564b2-d8ef-4384-8096-78b817438950)

- Checking the diffferent parts of package while selecting each of them :-
  
![M3_L2p9](https://github.com/user-attachments/assets/1ded7e18-d40d-4de6-be2d-f51e74d5f868)
![M3_L2p10](https://github.com/user-attachments/assets/9100f0b7-369d-4761-9af1-8c8060b405c9)
![M3_L2p11](https://github.com/user-attachments/assets/fbd569f3-94e4-4021-8a41-b00c90074edd)
![M3_L2p12](https://github.com/user-attachments/assets/9b7999e7-14ad-4914-be2c-5d4161c11f5b)
![M3_L2p13](https://github.com/user-attachments/assets/57a3131e-c2aa-4391-a422-87f956f65c91)
![M3_L2p14](https://github.com/user-attachments/assets/b332d797-1581-4d67-a5af-3545350c6883)
![M3_L2p15](https://github.com/user-attachments/assets/e9386b20-5273-48cc-bcbc-9d2012afe4f0)

### Material Definitions And Thermal Power Sources ###

- Setting up the monitor at die & substrate for thermal analysis :- 

![M3_L3p1](https://github.com/user-attachments/assets/4be6bfce-0215-4cb5-93e7-aa5c7a62406b)
![M3_L3p3](https://github.com/user-attachments/assets/8c3698eb-1c27-4b78-8787-c7ea5b85743e)
![M3_L3p4](https://github.com/user-attachments/assets/41baa6a9-cb71-4da2-b7ac-cd041f9a0596)
![M3_L3p5](https://github.com/user-attachments/assets/6ab12d5f-d718-4a39-93f5-aaab9c364584)
![M3_L3p6](https://github.com/user-attachments/assets/e05f0464-8ef4-4796-9acc-26ccfdf5f030)
![M3_L3p7](https://github.com/user-attachments/assets/1f7565c3-cab5-46ab-b6a6-1afba8003057)
![M3_L3p8](https://github.com/user-attachments/assets/531fa222-7691-4701-a397-b7b476857323)
![M3_L3p9](https://github.com/user-attachments/assets/cb8fe114-1cf5-4eba-9e16-cf4cd6947ee4)
![M3_L3p10](https://github.com/user-attachments/assets/6c181673-af04-4521-bdf8-b90ea0b0a953)

- Monitor are set now , which can be confirmed as below :- 

![M3_L3p11](https://github.com/user-attachments/assets/33a97f4e-4dc7-4408-9ac7-df2e34a26c64)

### Meshing And Running The Thermal Analysis ### 

- Creating the mesh :- 

![M3_L4p1](https://github.com/user-attachments/assets/e5420e55-d814-4c99-803e-720bb6aa2d90)

- Review for various mesh elements :-
  
![M3_L4p2](https://github.com/user-attachments/assets/e5db22f7-a0ea-469c-a7d5-643b828d347a)

- creating the setup for analysis purpose & validate :-

![M3_L4p3](https://github.com/user-attachments/assets/0b365409-90ba-4214-8f61-f184f936ae9d)
![M3_L4p4](https://github.com/user-attachments/assets/5089d04a-93c3-40c1-bb1c-e35314598b3e)

- If any mesh region is missed it can be added in following way :- 

![M3_L4p5](https://github.com/user-attachments/assets/a3c015d0-6e49-40a2-8c39-36c44a0125c1)
![M3_L4p6](https://github.com/user-attachments/assets/ecd26aeb-fdc1-42f2-bcfb-e6b68bf3e8bf)
![M3_L4p7](https://github.com/user-attachments/assets/be8aae05-37dd-41d8-b030-fee47fb2457c)

### Viewing Results And Exploring Other Package Types ###

- Setting up the plot to view the temperature :- 

![M3_L5p1](https://github.com/user-attachments/assets/41934ffd-18a8-4174-90f1-1978046bf15f)
![M3_L5p2](https://github.com/user-attachments/assets/6ff6fb09-d3e7-402d-b52b-9535a0339e90)
![M3_L5p3](https://github.com/user-attachments/assets/2fa41906-f0e9-465c-a617-927e0052f362)
![M3_L5p4](https://github.com/user-attachments/assets/3277a858-935c-439f-8097-d0bdab7eb4b6)

- Finally thermal analysis can viewed in following way :- 

![M3_L5p5](https://github.com/user-attachments/assets/6f7b1dc3-1dfb-4ca8-a7f7-df0041f79198)


## [Module 4] ## 

###  Introduction to Package Testing and Electrical Functionality Checks ### 

- **Multi-Stage Testing Process**<br>
  Testing ensures semiconductor reliability by detecting electrical, mechanical, and physical defects.<br>
  It begins at the foundry with wafer probe testing after front-end manufacturing.<br>
  Wafer sorting follows, selecting functional dies for packaging.<br>
  After package assembly at the OSAT stage, package-level testing checks for defects. Finally, System Level Testing (SLT)<br>
  evaluates real-world performance. Throughout, failure analysis helps refine processes and improve yield<br>
  
  ![ML4_L1p1](https://github.com/user-attachments/assets/cbdd5eda-8eec-4337-990f-dce336563aa2)

- **Package Testing**<br>
  as shown in figure below , after packaging in a cleanroom (ISO Class 6 & 7), chips are placed in package sockets for testing<br>
  AOST (Assembly Open and Short Test) – Verifies basic electrical connectivity to detect open or short circuits.<br>
  Burn-in Test – Applies thermal and voltage stress to identify early failures.<br>
  Final Test – Evaluates functionality, parametric performance and reliability across different temperatures (cold & hot tests).<br>
  
  ![ML4_L1p2](https://github.com/user-attachments/assets/6b21fe80-b52c-43ce-8d9f-95d2140352cc)

- **Overview of Assembly Open and Short Test (AOST)**<br>
  AOST detects electrical opens and shorts on package leads or balls.<br>
  Performed after Trim & Form (leadframe) or Singulation (BGA).<br>
  Catches major defects before products leave assembly.<br>
  Includes visual checks for damaged, missing, or misaligned leads/balls.<br>
  Identifies issues like HoP, bridging, NWO, die cracks, and warpage.<br>
  Uses automation for fast, accurate testing.<br>
  Devices are graded (1: Best, 2/3: Better, 4: Scrap) via PGSRT.<br>
  Improves yield and ensures only good units proceed.<br>
  
  ![ML4_L1p4](https://github.com/user-attachments/assets/852ca29e-4305-454f-9273-40def1a42c81)

### Reliability and Performance Testing of Semiconductor Packages ###

- **Reliability Testing in Semiconductors: Bathtub Curve & Burn-In Process**<br>

  The Bathtub Curve represents failure rates over time, starting with high early failures, followed by a stable useful life, and ending with wear-out failures.<br>
  Burn-In is a stress test done to screen out early-life failures by running devices under high temperature and voltage.<br>
  Burn-In Boards (BIBs) are used to hold multiple devices during this process and are built to withstand harsh conditions.<br>
  Burn-In Systems are chambers that control the testing environment, ensuring consistent stress application and monitoring.<br>
  The main goal is to remove weak units early, so only reliable devices enter the useful life phase, maximizing performance and longevity.<br>

  ![ML4_L2p1](https://github.com/user-attachments/assets/db460f37-befa-44cb-8db0-28624c6c102d)

- **Hot and Cold Temperature Testing**<br>

  The Final Test subjects devices to thermal extremes to uncover hidden or marginal defects.<br>
  Automated Test Equipment (ATE) with temperature-controlled handlers is used to apply cold and hot conditions, not ovens.<br>
  The Hot Test stresses devices at high temperatures, increasing the chance of detecting issues like leakage, timing failures, or marginal circuits.<br>
  The Cold Test challenges the device at low temperatures, where slow operation and threshold shifts can reveal otherwise hidden defects.<br>
  Together, these tests ensure the product is robust and performs reliably across its full specified temperature range.<br>

  ![ML4_L2p2](https://github.com/user-attachments/assets/ce3b1804-d549-4ee7-bb05-7de19ae5cd21)

- **ATE (Automatic Test Equipment) Testing Overview**<br>

  ATE automates the testing of semiconductor devices by applying test patterns to the Device Under Test (DUT).<br>
  It performs Parametric Tests (voltage/current checks), Functional Tests (behavior verification), and Speed Tests (timing performance).<br>
  Testing efficiency is measured by yield, test time, and test coverage.<br>

  ![ML4_L2p3](https://github.com/user-attachments/assets/24b029c6-dbfd-4e84-89f5-3cb7b13e2dbc)


## [Module 5] ## 

### Introduction to Package Cross-Section Modeling in ANSYS Electronics Desktop (AEDT) ### 

![M5_L1p1](https://github.com/user-attachments/assets/cf56e936-ce4f-442b-a382-cafa58c6a717)

- In this lab , 3D package is being created from stratch (unlike Module 2 where package was directly import) 

  -  Ansys Electronics Desktop (AEDT) was used to virtually design a semiconductor wire bond package up to the molding stage.
  -  The process began with defining the die and substrate geometry using AEDT’s 3D layout tools, followed by assigning realistic material properties. 
  -  A die attach layer was placed beneath the die to replicate adhesive bonding, with appropriate thermal characteristics.
  -  Bond pads were then created on both the die and substrate, and gold wire bonds were added to establish electrical connections. 
  -  The entire structure was encapsulated with a mold compound to provide mechanical protection and thermal insulation.
  -  The final model was verified for geometry accuracy, correct layer stacking, and material assignments. 
  -  Each step was visualized in AEDT’s 3D simulation environment, with key stages documented through screenshots.

### Creating the Die and Substrate in AEDT ### 

![M5_L2p1](https://github.com/user-attachments/assets/23deeb12-2dee-469f-9fdf-0339f1e0c7e9)
![M5_L2p2](https://github.com/user-attachments/assets/c3529189-fd19-43e9-990b-45648b365275)
![M5_L2p3](https://github.com/user-attachments/assets/28bc8048-9803-4b53-a0a8-a744e926af5f)
![M5_L2p4](https://github.com/user-attachments/assets/3f888c2a-4aea-4994-990d-6bc7dadc7799)
![M5_L2p5](https://github.com/user-attachments/assets/13cfe43b-6af0-49c0-87d9-a1dae004bc38)
![M5_L2p6](https://github.com/user-attachments/assets/7623e7d1-4fc0-4a03-a3fd-6ebb2335fb94)
![M5_L2p7](https://github.com/user-attachments/assets/aaa00d5c-616e-483f-b2c1-56d784ba3467)
![M5_L2p8](https://github.com/user-attachments/assets/86116aee-300f-4683-a3a9-35efdb175d42)
![M5_L2p9](https://github.com/user-attachments/assets/32a7e77c-8c37-405c-af07-fab907cdf295)
![M5_L2p10](https://github.com/user-attachments/assets/611a8d24-853a-49a4-bbc9-652cc6110122)
![M5_L2p11](https://github.com/user-attachments/assets/3d5c54d3-f4cc-4275-a5e3-3c416379e4b4)
![M5_L2p12](https://github.com/user-attachments/assets/acd3c73e-f18b-47e4-b4d2-173cb3ee1ec9)
![M5_L2p13](https://github.com/user-attachments/assets/8447e98c-0d40-46b2-8546-1c1e90e1918b)

### Material Definitions And Thermal Power Sources ###

![M5_L3p1](https://github.com/user-attachments/assets/2328527f-36c2-4aab-82ad-e2ce5bee0b37)
![M5_L3p2](https://github.com/user-attachments/assets/44311920-437e-4985-b461-2063c9cb656a)
![M5_L3p3](https://github.com/user-attachments/assets/86a5a03b-5042-4904-8fc4-f9b274972dd0)
![M5_L3p4](https://github.com/user-attachments/assets/3a68010f-85e4-4752-ac22-02591e4f4cb2)
![M5_L3p5](https://github.com/user-attachments/assets/838f30ea-bead-4173-8618-3a545a6c2e95)
![M5_L3p6](https://github.com/user-attachments/assets/4c818c17-98a7-41c7-a80e-085db7f353c6)

### Wire Bond Creation and Material Assignment ### 

![M5_L4p1](https://github.com/user-attachments/assets/7e4dd4c8-d9f2-40e6-9522-6e5d6abce530)
![M5_L4p2](https://github.com/user-attachments/assets/ac9ecba6-0450-45d2-bb60-33b0b9eccd66)

### Applying Mold Compound and Finalizing the Package Model  ### 

![M5_L5p1](https://github.com/user-attachments/assets/2388b1f3-119a-42ff-bae1-1f8bcb8521ba)
![M5_L5p2](https://github.com/user-attachments/assets/b2de161c-fa8f-4969-8d87-e906169a4b23)


# Acknowledgement #

Grateful thanks to Mr. Kunal Ghose from VLSI System Design (VSD) for organizing and leading the Packaging Fundamentals of Design and Technology Workshop.<br>

Sincere appreciation to Prof. Tarun Agarwal from IIT Gandhinagar for delivering insightful and engaging lectures that enhanced the overall learning experience.<br>

Their contributions made the workshop a valuable journey into advanced semiconductor packaging technologies.<br>

