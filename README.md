# Medicare-Project-using-Pyspark
- PredictIing the Average Medicare Standardized Payment Amount for the medicare service.
Medicare is the federal government plan in the U.S. for paying certain hospital and medical expenses for elderly persons qualifying under the plan. It is available for people age 65 or older, younger people with disabilities and people with End Stage Renal Disease (permanent kidney failure requiring dialysis or transplant). Medicare has two parts, Part A (Hospital Insurance) and Part B (Medicare Insurance). You are eligible for premium-free Part A if you are age 65 or older and you or your spouse worked and paid Medicare taxes for at least 10 years.
Medicare Physician & Other Practitioners - by Geography and Service Data Dictionary :
1) Rndrng_Prvdr_Geo_Lvl :
Variable Name : Geography Level

Identifies the level of geography that the data in therow has been aggregated. A value of 'State' indicates the data in the row is aggregated to a single state identified in the Rendering Provider State column for a given HCPCS Code Level. A value of 'National' indicates the data in the row is aggregated across all states for a given HCPCS Code Level.

2) Rndrng_Prvdr_Geo_Cd :
Variable Name : Rendering Provider Geography Code

FIPS code of the referring provider state. This variable is blank when reported at the national level.

3) Rndrng_Prvdr_Geo_Desc :
Variable Name : Rendering Provider Geography Description

The state name where the provider is located, as reported in NPPES. The values include the 50 United States, District of Columbia, U.S. territories, Armed Forces areas, Unknown and Foreign Country. Data aggregated at the National level are identified by the word 'National'.

4) HCPCS_Cd :
Variable Name : HCPCS Code

HCPCS code used to identify the specific medicalservice furnished by the provider. HCPCS codes include two levels. Level I codes are the Current Procedural Terminology (CPT) codes that are maintained by the American Medical Association and Level II codes are created by CMS to identify products, supplies and services not covered by the CPT codes (such as ambulance services). CPT codes, descriptions and other data only are copyright 2016 American Medical Association. All rights reserved. CPT is a registered trademark of the American Medical Association (AMA).Please review the complete CMS AMA CPT License agreement which is presented to users when accessing the data. For additional information on HCPCS codes,visit the HCPCS general information page.

5) HCPCS_Desc :
Variable Name : HCPCS Description

Description of the HCPCS code for the specific medical service furnished by the provider. HCPCS descriptions associated with CPT codes are consumer friendly descriptions provided by the AMA. CPT Consumer Friendly Descriptors are lay synonyms for CPT descriptors that are intended to help healthcare consumers who are not medical professionals understand clinical procedures on bills and patient portals. CPT Consumer Friendly Descriptors should not be used for clinical coding or documentation. All other descriptions are CMS Level II descriptions provided in long form. Due to variable length restrictions, the CMS Level II descriptions have been truncated to 256 bytes.As a result, the same HCPCS description can be associated with more than one HCPCS code. For complete CMS Level II descriptions, please visit the HCPCS Release Code Sets page.

6) HCPCS_Drug_Ind :
Variable Name : HCPCS Drug Indicator

Identifies whether the HCPCS code for the specific service furnished by the provider is a HCPCS listed on the Medicare Part B Drug Average Sales Price (ASP) File.Please visit the ASP drug pricing page for additional information.

7) Place_Of_Srvc :
Variable Name : Place of Service

Identifies whether the place of service submitted onthe claims is a facility (value of ‘F’) or non-facility (value of ‘O’). Non-facility is generally an office setting; however other entities are included in non-facility. The following values are entities included in facility and nonfacility:

8) Tot_Rndrng_Prvdrs :
Variable Name : Number of Providers

Number of providers within HCPCS code and place of service.

9) Tot_Srvcs :
Variable Name : Number of Services

Number of services provided; note that the metrics used to count the number provided can vary from service to service.

10) Tot_Benes :
Variable Name : Number of Medicare Beneficiaries

Number of distinct Medicare beneficiaries receiving the service for each Rndrng_Prvdr_Geo_Desc and HCPCS_Cd, Place_Of_Srvc.

11) Tot_Bene_Day_Srvcs :
Variable Name : Number of Distinct Medicare Beneficiary/Per Day Services

Number of distinct Medicare beneficiary/per day services. Since a given beneficiary may receive multiple services of the same type (e.g., single vs. multiple cardiac stents) on a single day, this metric removes double-counting from the line service count to identify whether a unique service occurred.

12) Avg_Sbmtd_Chrg :
Variable Name : Average Submitted Charge Amount

Average of the charges that providers submit for the service.

13) Avg_Mdcr_Alowd_Amt :
Variable Name : Average Medicare Allowed Amount

Average of the Medicare allowed amount for the service. Medicare allowed amounts includes the amount Medicare pays, the deductible and coinsurance amounts that the beneficiary is responsible for paying, and any amounts that a third party is responsible for paying.

14) Avg_Mdcr_Pymt_Amt :
Variable Name : Average Medicare Payment Amount

Average amount that Medicare paid after deductible and coinsurance amounts have been deducted for the line item service.

15) Avg_Mdcr_Stdzd_Amt :
Variable Name : Average Medicare Standardized Payment Amount

Average amount that Medicare paid after beneficiary deductible and coinsurance amounts have been deducted for the line item service and after standardization of the Medicare payment has been applied. Standardization removes geographic differences in payment rates for individual services, such as those that account for local wages or input prices and makes Medicare payments across geographic areas comparable, so that differences reflect variation in factors such as physicians’ practice patterns and beneficiaries’ ability and willingness to obtain care. Additional information on the standardization of Medicare payments can be found in the “Geographic Variation Public Use File: Technical Supplement on Standardization.”
