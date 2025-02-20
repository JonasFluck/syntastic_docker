# Syntastic docker version
This is a demo on how to setup syntastic with docker.

Syntastic is a project for simulating drug events based on SNPs (Single Nucleotide Polymorphisms) for each individual.  
This is done in a probabilistic way.  
Syntastic assumes an input of patient data that specifies the SNPs of each patient and will generate two .csv output files.


## How it works

to run this demo application:
1. Clone this repository
2. Run:

        docker compose pull
        docker compose up -d
Thats it !
## Configuration
There are two important files to consider when working with syntastic:
+ <span style="color: #87CEEB;">input.csv</span>
+ <span style="color: #87CEEB;">config.json</span>

These must always be located in the data folder.

### input.csv
### config.json
### config.json
| Parameter                              | Impact                                      | Type    | Default |
|----------------------------------------|---------------------------------------------|---------|---------|
| minAge                                 | Minimum age of generated patients           | Integer |Not set  |
| maxAge                                 | Maximum age of generated patients           | Integer |Not set  |
| maxDrugs                               | Maximum number of drugs                     | Integer |         |
| snpsPerDrugType                        | SNPs per drug type                          | Integer |         |
| percentageOfSnpsForDrugPerDrugType     | Percentage of SNPs for drug per drug type   | Integer |         |
| baseDrugEffectiveness                  | Base drug effectiveness                     | Double  |         |
| negativePriorDrugEvent                 | Negative prior drug event                   | Double  |         |
| positivePriorDrugEvent                 | Positive prior drug event                   | Double  |         |
| gender                                 | Gender                                      | List    |         |
| countries                              | List of countries                           | List    |         |
| positiveResponseAnotherDrug            | Positive response to another drug           | Double  |         |
| negativeResponseAnotherDrug            | Negative response to another drug           | Double  |         |