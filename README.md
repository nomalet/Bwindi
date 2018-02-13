# Bwindi Community Hospital

## Introduction

### Background

Bwindi Community Hospital (BCH) is a Not-For-Profit hospital in south-west Uganda, providing healthcare to rural and isolated communities. Although BCH actively fundraises to ensure the hospital running costs are covered, only 8% of the hospital's funding comes from the Ugandan government, which means the hospital must charge patients at the point of healthcare delivery to ensure that all costs are covered.

The majority of BCH patients are subsistence farmers who earn low to no money, so they avoid seeking healthcare fearing the costs. In order to mitigate this problem and encourage patients to seek healthcare and improve the overall community access to healthcare, BCH has set up an insurance plan called eQuality. This plan allows patients to join via a Bataka group (local community groups) whereby the Bataka group joins in its entirety.

BCH estimates that 90% of the daily visits are by eQuality members. The remaining 10% are from one-off visits and those who can afford to not have insurance. However, BCH also believes that the eQuality members are generally from the immediate vicinity and it would like to expand its offering of eQuality to the wider community by contacting individuals to persuade them to join.

### Problem Statement

As the majority of people living in rural Uganda own a basic mobile phone that is at least capable of receiving SMS messages, BCH intends to send out SMS messages to the wider community to advertise eQuality and encourage people to join.

Can BCH identify the type of person or the type of Bataka group that might take out membership in eQuality in order to contact them?

### Strategy

The strategy is to identify the type of individual who is already an eQuality member compared to those individuals who are not. Using this profile, individuals or households will be identified that might be open to becoming members.

As the data is labelled with discrete values, this will be best approached as a classification problem.

### Data and Data Sources

BCH manages multiple databases, but one of these will be used for this project will be the hospital's patient database.

The patient database contains personal, financial, location and health details of the individuals. It also contains details about households which helps to connect the patient to the community database.

### Potential Pitfalls

###### Patient Database
- The database might not contain sufficient non-members to correctly predict a member vs non-member.
- The data might be not have been accurately or consistently recorded over time.

## Data Dictionary

### Scheme History Data


SchemeHistoryId: ID for the subscription entry date and batch of Members <br>
OrganisedGroupId: ID for the Bataka group that the members belong to <br>
PInsuranceSchemeId: ID for insurance scheme designation - this is eQuality for the entire table <br>
SubscriptionChannelId: Channel through which members subscribed <br>
SubscriptionDate: Date that the batch of members subscribed to eQuality <br>
Duration: Duration, in months, that the batch of members subscribed to eQuality <br>
MembersWhoEnrolled: ID for each member who enrolled in eQuality on the Subscription Date <br>

### Member Data


MemberId : ID number for individual registered on the system (this does not imply membership in the insurance) <br>
HouseholdId : ID for the household where all individuals are registered  <br>
CollectionYear : Year of data collection  <br>
MemberType : Head of the household or not  <br>
MemberBirthName : First name of individual (Ugandans do not use family names - they simply use either given name)  <br>
MemberOtherNames : Second name of individual (Ugandans do not use family names - they simply use either given name)  <br>
MemberGender : Male or Female  <br>
MemberDateOfBirth : Date of birth in yyyy-mm-dd format  <br>
PlaceOfBirth : Location of birth of the member  <br>
DateOfRegistration : Date that the individual's details were registered in the hospital database  <br>
SubscriptionDate : If the member paid insurance fees, the date this was done  <br>
Duration : Duration of insurance, usually 4 month intervals  <br>
FatherAlive : Father of individual is still alive  <br>
MotherAlive : Mother of individual is still alive  <br>
FatherWithChildren : Father of household is living with the children  <br>
MotherWithChildren : Mother of household is living with the children  <br>
SleepsUnderITN : Individual sleeps under a insecticide treated mosquito net  <br>
HasChildHealthCard : Child has a health card  <br>
EverTestedForHIV : Individual has been tested previously for HIV  <br>
MUAC : Measure for malnutrition  <br>
CoughMoreThanThreeWeeks : Individual coughs more than three weeks  <br>
CompletedDTP3 : Individual has been inoculated for DTP  <br>
CompletedMeasles : Individual has been inoculated for measles  <br>
GivenNewChildHealthCard : Child given a new health card  <br>
WeightAtRegistration : Individual weight at registration  <br>
HeightAtRegistration : Individual height at registration  <br>
NoChildrenBorn : Number of children born to an individual  <br>
NoChildrenAlive : Number of children alive belonging to an individual  <br>
CurrentlyPregnant : Individual is pregnant at the time of registration  <br>
CurrentlyBFeeding : Individual is breastfeeding at the time of registration  <br>
EDW_Epilepsy : Existing disability Epilepsy  <br>
EDW_Diabetes : Existing disability Diabetes  <br>
EDW_ChronicRespiratoryDisease : Existing disability Chronic Respiratory Disease  <br>
EDW_HIV : Existing disability HIV  <br>
EDW_CerebralPalsy : Existing disability Cerebral Palsy  <br>
EDW_OtherMusculoskeletalDisability : Existing disability Musculoskeletal  <br>
EDW_OtherLearningDifficulty : Existing disability Learning Difficulty  <br>
EDW_Tuberculosis : Existing disability Tuberculosis  <br>
EDW_HeartDisease : Existing disability Heart Disease  <br>
EDW_Malnutrition : Existing disability malnutrition  <br>
OtherMedicalIssue : Existing disability other than those listed  <br>
EducationLevelName : Education level  <br>
DVision : Disability with Vision  <br>
DHearing : Disability with Hearing  <br>
DArmsHands : Disability with Arms or Hands  <br>
DFeetLegs : Disability with Feet or Legs  <br>
MalariaTimes : Number of times contracted malaria  <br>
KnowWhereTestHIV : Individual knows where to get an HIV test  <br>
KnowWhereGetARVs : Individual knows where to get ARV (antiretrovirals)  <br>
OrganisedGroupName : Bataka groups, the local political groups that members can use in order to purchase eQuality insurance <br>
EthnicGroupName : Ethnic group to which the individual belongs  <br>
HealthInsuranceGroupName : Name of Health Insurance that individual owns (BCH provides eQuality insurance) <br>
SubscriptionChannelName : Method by which individual has subscribed to health insurance  <br>
VillageName : Village where the individual lives  <br>
ParishName : Parish where the individual lives  <br>
SubcountyName : Subcounty where the individual lives  <br>
ZOrdinate : GPS Coordinate of household  <br>
XOrdinate : GPS Coordinate of household  <br>
YOrdinate : GPS Coordinate of household  <br>

### Household Data

HouseholdId : ID for household  <br>
MemberId : ID number for individual registered on the system  <br>
OrganisedGroupName : Bataka groups, the local political groups that members can use in order to purchase eQuality insurance  <br>
CollectionYear : Year of data collection  <br>
IncomeSourceName : Source of household income  <br>
MonthlyIncome : Amount of monthly household income  <br>
FoodEnough : Is food enough to feed the household  <br>
DaysFoodNotEnough : Days that food has been short in the household  <br>
FoodRight : Food is correct nutritionally  <br>
DaysFoodNotRight : Days that the food available was incorrect nutritionally  <br>
TypeDwellingUnitName : Household dwelling type  <br>
ConditionDwellingUnitName : Condition of the dwelling  <br>
TenureDwellingUnitName : Tenure of the dwelling  <br>
LightingFuel : Fuel used for lighting  <br>
CookingFuel : Fuel used for cooking  <br>
WaterSourceName : Source of household water  <br>
ToiletFacilityName : Type of toilet facility  <br>
InformationSourceName : The information source for the household  <br>
VillageName : Village where the household is  <br>
ParishName : Parish where the household is  <br>
SubcountyName : Subcounty where the household is <br>


# Table of Contents
1  Bwindi Community Hospital
1.1  Introduction
1.1.1  Background
1.1.2  Problem Statement
1.1.3  Strategy
1.1.4  Data and Data Sources
1.1.5  Potential Pitfalls
1.2  Data Dictionary
1.2.1  Scheme History Data
1.2.2  Member Data
1.2.3  Household Data
2  Libraries
3  MySQL Hospital Database
3.1  Database Connection Configuration
3.2  Insurance Scheme History
3.3  Member Data
3.4  Household Data
3.5  Member and Household Data
3.6  Member Lists
3.6.1  Member List 2009
3.6.2  Member List 2010
3.6.3  Member List 2011
3.6.4  Aggregate Member List
3.7  Household Lists
3.7.1  Household List 2009
3.7.2  Household List 2010
3.7.3  Household List 2011
3.7.4  Aggregate Household List
4  Assemble The Dataframes
4.1  Subscription History Data
4.1.1  Splitting and Melting
4.1.2  Cleaning the MemberId
4.2  QC Against ORGA Groups
4.2.1  Eliminating Duplicates
4.3  Create a History Dataframe Grouped By Member
4.4  Merge Dataframes History, Member, Household
4.4.1  Prepare Member Dataframe
4.4.2  Merge Member_master With Member
4.4.3  Merge History and Member and Household
5  Data Cleaning
5.0.1  Cleanup of Strings and Values
5.0.2  Data Imbalance
5.0.3  Engineered Features
5.0.4  Drop Missing Values
5.1  Create Target Features
5.1.1  eQuality Subscriber or Not
5.1.2  Subscriber Loyalty Ranking
6  EDA
6.1  Ungrouped Dataframes
6.2  Dataframes Grouped by Organised Group
6.2.1  Pre-Process Dataframes
6.2.2  Targets After Grouping
6.2.3  Look at Features
6.2.4  Feature Correlations
6.2.4.1  SignUp
6.2.4.2  Loyalty
6.2.5  Mapping
6.2.5.1  Targets
6.2.5.2  Demographics
7  Modelling
7.1  SignUp Model
7.1.1  Important Features
7.1.1.1  Preprocessing
7.1.1.2  TPOT Model Selector
7.1.1.3  Logistic Regression
7.1.1.4  Decision Tree
7.1.2  Pipeline
7.1.2.1  Grid Search
7.1.2.2  Logistic Regression
7.1.2.3  Random Forest
7.1.2.4  Extra Trees Classifier
7.2  Loyalty Model
7.2.1  Important Features
7.2.1.1  Preprocessing
7.2.1.2  TPOT Model Selector
7.2.1.3  Logistic Regression
7.2.1.4  Decision Tree
7.2.2  Pipeline
7.2.2.1  Grid Search
7.2.2.2  Logistic Regression
7.2.2.3  Random Forest
7.2.2.4  Extra Trees Classifier
8  Conclusion
9  Recommendations
