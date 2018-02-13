# Bwindi Community Hospital

## Introduction

### Background

Bwindi Community Hospital (BCH) is a Not-For-Profit hospital in south-west Uganda, providing healthcare to rural and isolated communities. Although BCH actively fundraises to ensure the hospital running costs are covered, only 8% of the hospital's funding comes from the Ugandan government, which means the hospital must charge patients at the point of healthcare delivery to ensure that all costs are covered.

The majority of BCH patients are subsistence farmers who earn low to no money, so they avoid seaking healthcare fearing the costs. In order to mitigate this problem and encourage patients to seak healthcare and improve the overall community access to healthcare, BCH has set up an insurance plan called eQuality. This plan allows patients to join via a Bataka group (local community groups) whereby the Bataka group joins in its entirety.

BCH estimates that 90% of the daily visits are by eQuality members. The remaining 10% are from one-off visits and those who can afford to not have insurance. However, BCH also believes that the eQuality members are generally from the immediate vicinity and it would like to expand its offering of eQuality to the wider community by contacting individuals to pursuade them to join. 

### Problem Statement

As the majority of people living in rural Uganda own a basic mobile phone that is at least capable of receiving SMS messages, BCH intends to send out SMS messages to the wider community to advertise eQuality and encourage people to join.

Can BCH identify the type of person or the type of Bataka group that might take out membership in eQuality in order to contact them?

### Strategy

The strategy is to identify the type of individual who is already an eQuality member compared to those individuals who are not. Using this profile, individuals or households will be identified that might be open to becoming members.

Possible modelling techniques:
- Classifying
- Clustering
- Bayesian modelling

### Data and Data Sources

BCH manages multiple databases, but one of these will be used for this project will be the hospital's patient database.

The patient database contains personal, financial, location and health details of the individuals. It also contains details about households which helps to connect the patient to the community database.

### Potential Pitfalls

###### Patient Database
- The database might not contain sufficient non-members to correctly predict a member vs non-member.
- The data might be not have been accurately or consistently recorded over time.

## Data Dictionary

### Scheme History Data - FIX THIS


SchemeHistoryId: ID for the subsciption entry date and batch of Members <br>
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
WeightAtRegistration : Individual weigth at registration  <br>
HeightAtRegistration : Individual heigth at registration  <br>
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
EDW_Malnutrition : Existing disability Malnitrition  <br>
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
SubscriptionChannelName : Method by which individual has subsribed to health insurance  <br>
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
CookingFuel : Fueld used for cooking  <br>
WaterSourceName : Source of household water  <br>
ToiletFacilityName : Type of toilet facility  <br>
InformationSourceName : The information source for the household  <br>
VillageName : Village where the household is  <br>
ParishName : Parish where the household is  <br>
SubcountyName : Subcounty where the household is <br> 
