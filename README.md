# Starbucks capstone Challenge 

the link to the medium is https://medium.com/@quantum360ai/what-are-the-chances-that-you-will-respond-to-an-starbucks-offer-8e8a2eb51a61

Structure of the file is 
## Motivation 

I did this project to check my knowledge and confidence in the case of the real world problem 

## context
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the challenge to solve with this data set.

The task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

Every offer has a validity period before the offer expires. As an example, a BOGO offer might be valid for only 5 days. In the data set that informational offers have a validity period even though these ads are merely providing information about a product; for example, if an informational offer has 7 days of validity, you can assume the customer is feeling the influence of the offer for 7 days after receiving the advertisement.


## The Goal 

The basic task is to use the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer.



## File Description 

First lets see the structure of the file :-

    ├── data                   
    │   ├── offer
    │   ├── offer_norec_comp
    │   |── offer_record
    │   |── offer_record_norec_comp    
    │   |── person_all_information
    │   |── person_offer_demographic
    │   |── portfolio.json
    │   |── transaction_gen
    │   |── transcript_new_2   
    | 
    ├── Starbucks_capstane_notebook.ipynb   # contain main file 
    |
    ├── filename4.pkl  
    │                 # Trained ML model  
    |── article.pdf  # main pdf file that contain article
    |                                      
    └── README.md     # all the contains 

<a name ="run"></a>

## Dataset overview
* The program used to create the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers.

* Each person in the simulation has some hidden traits that influence their purchasing patterns and are associated with their observable traits. People produce various events, including receiving offers, opening offers, and making purchases.

* As a simplification, there are no explicit products to track. Only the amounts of each transaction or offer are recorded.

* There are three types of offers that can be sent: buy-one-get-one (BOGO), discount, and informational. In a BOGO offer, a user needs to spend a certain amount to get a reward equal to that threshold amount. In a discount, a user gains a reward equal to a fraction of the amount spent. In an informational offer, there is no reward, but neither is there a requisite amount that the user is expected to spend. Offers can be delivered via multiple channels.
    
* The basic task is to use the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer.


## Data Dictionary

profile.json
> Rewards program users (17000 users x 5 fields)
 > * gender: (categorical) M, F, O, or null
 > * age: (numeric) missing value encoded as 118
 > * id: (string/hash)
 > * became_member_on: (date) format YYYYMMDD
 > * income: (numeric)
 

### portfolio.json
> Offers sent during 30-day test period (10 offers x 6 fields
 > * reward: (numeric) money awarded for the amount spent
 > * channels: (list) web, email, mobile, social
 > * difficulty: (numeric) money required to be spent to receive reward
 > * duration: (numeric) time for offer to be open, in days
 > * offer_type: (string) bogo, discount, informational
 > * id: (string/hash)

 ### transcript.json
 > Event log(306648 events * 4 fields)
  > * person: (string/hash)
  > * event: (string) offer received, offer viewed, transaction, offer completed
  > * value: (dictionary) different values depending on event type
     > * offer id: (string/hash) not associated with any "transaction"
     > * amount: (numeric) money spent in "transaction"
     > * reward: (numeric) money gained from "offer completed"
  > * time: (numeric) hours after start of test


  ## Licence 
     apache licence 2.0
  ## Author 
     kartikey shaurya 
  
  ## Acknowledgement 
     First of all thanks to Udacity for this wonderful oppertunity provided to work on something  

     Also, none of less thanks to starbucks for providing the dataset

