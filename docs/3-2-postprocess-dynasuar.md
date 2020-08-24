# **Dynasaur**

Dynasaur Input files are written in json. 

!!! tip "JSON Tip" 
        
    If you change something in a big file, it can help to use a json validator - e.g. https://jsonlint.com/

### Object.def

The object definition file contains information about the simulated models and defines identifiers which are further used within the calculation routines.

For further details, look at the [Dynasaur Wiki](https://gitlab.com/VSI-TUGraz/Dynasaur/-/wikis/Object-Definition-File)


### Calculation_procedure.def

As the name say, all calculation procedures, defines what we want to do with the outputs

Several standard functions are implemented, so that we can easily define which object should be used for specific criteria (e.g. HIC calculation, quality criteria), or channels (Data Visualisation - e.g. which CFC filter should be applied on the acceleration signals)

For further details, look at the [Dynasaur Wiki](https://gitlab.com/VSI-TUGraz/Dynasaur/-/wikis/Calculation-Procedure-Definition-File)
