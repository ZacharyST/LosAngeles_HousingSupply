# LosAngeles_HousingSupply
Merges 3 datasets from Abundant Housing LA (housing supply, American Community Survey, Zillow rent information)

The three datasets are provided by Anthony Dedousis via Tableau: https://public.tableau.com/profile/anthony.dedousis#!/.  As of 09.24.2019, he is Director of Research and Analysis at Abundant Housing LA.

Datasets:
   ACS - American Community Survey neighborhood-level data on population, number of households, race, rent/income ratio, income, unemployed, rent-burdened (more info here: https://www.census.gov/data/developers/data-sets/acs-5year.html)

   Housing Supply by Neighborhood - number of multifamily and single-family homes by neighborhood in LA - original source is the LA County Assessor's Office (http://maps.assessor.lacounty.gov/GVH_2_2/Index.html?configBase=http://maps.assessor.lacounty.gov/Geocortex/Essentials/REST/sites/PAIS/viewers/PAIS_hv/virtualdirectory/Resources/Config/Default).  I'd take the multifamily number with a BIG grain of salt - filtering the original dataset was hard and I'm pretty sure my teammate excluded apartments in mixed-use buildings

   Zillow - ZRI (Zillow Rent Index) estimating monthly inflation-adjusted rents by neighborhood (https://www.zillow.com/research/data/)

HousingSupply_Merge_v1.R standardizes column names, reshapes two of the datasets, and merges Zillow and ACS with the housing supply dataset.  

Unit of analysis is the neighborhood-year.  
