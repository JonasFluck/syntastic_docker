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
| Parameter | Impact | Type | Default |
|----------|----------|----------|----------|
| Data 1   | Data 2   | Data 3   |Data 3   |
| Data 4   | Data 5   | Data 6   |Data 6   |