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
All parameters are optional
| Parameter                              | Impact                                      | Type    | Default |
|----------------------------------------|---------------------------------------------|---------|---------|
| minAge                                 | Minimum age of generated patients           | Integer |Not set  |
| maxAge                                 | Maximum age of generated patients           | Integer |Not set  |
| maxDrugs                               | Maximum number of drugs                     | Integer |  5       |
| snpsPerDrugType                        | SNPs per drug type (SNPs that will have an effect on the response of the drugtype)                         | Integer |         |
| percentageOfSnpsForDrugPerDrugType     | Percentage of SNPs for drug per drug type   | Integer |  80       |
| baseDrugEffectiveness                  | Base drug effectiveness                     | Double  |   0.5      |
| negativePriorDrugEvent                 | Negative prior drug event decreases chance of next drug having positive response by...  | Double  |  0.1       |
| positivePriorDrugEvent                 | Negative prior drug event decreases chance of next drug having positive response by...  | Double  |  0,.1       |
| gender                                 | Gender                                      | String ("MALE" or "FEMALE")  | Not Set (means both are included)|
| countries                              | List of countries                           | List    |  All available |
| positiveResponseAnotherDrug            | If prior response was positive chance to order another drug| Double  | 0.05 |
| negativeResponseAnotherDrug            | If prior response was negative chance to order another drug| Double  | 0.8  |

```json
{
    "minAge":14,
    "maxAge":90,
    "maxDrugs":3,
    "snpsPerDrugType":100,
    "percentageOfSnpsForDrugPerDrugType":80,
    "baseDrugEffectiveness":0.5,
    "negativePriorDrugEvent":-0.1,
    "positivePriorDrugEvent":0.1,
    "gender":"MALE",
    "countries":["France, Spain"],
    "positiveResponseAnotherDrug": 0.05,
    "negativeResponseAnotherDrug":0.8
}
```