#### Obtaining Data
There are two APIs I used to obtain data for my study:

I used the [Pokémon TCG API](https://docs.pokemontcg.io/) to retrieve all data regarding both cards and sets. The card data took 31 calls to the API, each containing 250 observations. The set data took one call. To see the query parameters and how the calls to this API were made, please look at the first few code blocks of my sourcecode.Rmd file.
 
I used the [PokéAPI](https://pokeapi.co/) to retrieve data on Pokémon character names. This is used to help with the construction of one predictor variable (discussed later), but not as a predictor itself. Each call only allows for information on one character at a time. Thus, I had to make 1085 calls to the API. To see the query parameters and how the calls to this API were made, please look at the first few code blocks of my sourcecode.Rmd file.

#### About Reproducibility

 The Pokémon TCG API refreshes their price data daily. Thus, reproducing this study while requesting data live from the API is impossible. To make my study reproducible, I have saved the data I requested from the API on the day the report was published (May 7,2024). I stored this data in the repository of this project's github and I have included a reproducible version of my source code titled "sourcecode-reproducible". The only differences between these versions is that the reproducible version loads the data from the github while the regular version makes live requests to the API. Thus, to examine the process of requesting data, please refer to the sourcecode.Rmd file. However, to reproduce the results of this study, please run the code in the sourcecode-reproducible.Rmd file.
