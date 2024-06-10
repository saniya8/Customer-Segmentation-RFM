# Customer-Segmentation-RFM

## Summary

This project performs customer segmentation analysis in Python using the recency, frequency, monetary (RFM) model to classify customers into 11 distinct segments.

## How To Run 

**Input:** 
- customer_segmentation_rfm.ipynb
- customer_segmentation_data_input.csv
  
**Output:**
- customer_segmentation_rfm_output.csv, which will automatically download to your project folder once code is run

**Results:**
- customer_segmentation_rfm_dashboard, where I've created a Tableau dashboard that visually displays the results in customer_segmentation_rfm_output.csv 

**Running The Code:**
1. Download all the files from the repository. The specific ones needed to run the code are:
   - customer_segmentation_rfm.ipynb (Jupyter notebook with my Python code)
   - customer_segmentation_data_input.csv (CSV input file with customer data)
2. Open customer_segmentation_rfm.ipynb in Jupyter notebook and click run

## About The Project

**Problem Statement:**

It is necessary for businesses to understand how to group their customers based similar characteristics in order to determine the value derived from them, understand their buying habits, target them more effectively, and align the business strategy with customer needs. 

**Objective:**

The objective of this project is to segment customers using the RFM model. The segments can be used to identify the most valuable customers (highest recency, highest frequency, highest monetary RFM scores) and least valuable customers (lowest recency, lowest frequency, and lowest monetary RFM scores). 

**Customer Segmentation:**

Customer segmentation refers to splitting up customers into different groups, or segments, based on specific common characteristics they share. In this project, the common characteristics are the recency, frequency, and monetary values. The result of customer segmentation is distinct clusters of customers with their unique, identifiable characteristics. 

**RFM Model:**

The recency, frequency, monetary (RFM) model is a model that helps perform customer segmentation. 
Recency: how recently did the customer make a purchase?
Frequency: how often does a customer make a purchase?
Monetary: how much money does a customer spend when making a purchase?

This model first involves calculating the recency, frequency, and monetary values. For example, a recency of 3, frequency of 5, and monetary of 4090.88 indicates that the most recent purchase from the customer was 3 days ago, they have purchased 5 times from the company, and their cumulative spending is $4090.88. 

After calculating the recency, frequency, and monetary values for all the customers, the model classifies each of these values into their respective bins based on, in this project, the quintile they are in. In this case, there are five bins for recency, five bins for frequency, and five bins for monetary. The concatenation of the bin numbers for the recency, frequency, and monetary values provides the RFM score. For example:
- An RFM score of 432 shows that the customer's recency value is in bin 4, the customer's frequency value is in bin 3, and the customer's monetary value is in bin 2.
- An RFM score of 555 shows that the customer's recency value is in bin 5, the customer's frequency value is in bin 5, and the customer's monetary value is in bin 5. This is the most valuable customer, with a high recency score (very recently purchased an item), a high frequency score (purchases very often), and a high monetary score (spends a lot on purchases).
- An RFM score of 111 shows that the customer's recency value is in bin 1, the customer's frequency value is in bin 1, and the customer's monetary value is in bin 1. This is the least valuable customer, with a low recency score (purchased an item a very long time ago), a low frequency score (purchases very rarely), and a high monetary score (spends very little on purchases).

The recency, frequency, and monetary scores are all either 1, 2, 3, 4, 5 since each has five bins. Each of the 125 possible RFM scores are classified into a particular segment. There are 11 different segments in total. This is how customers obtain their segment classification. For example:
- An RFM score of 432 corresponds to the segment called "Potential Loyalists".
- An RFM score of 553 also corresponds to the segment called "Potential Loyalists".
- Hence, any customers with an RFM score of 432 or 553 will fall into the same segment of Potential Loyalists.

Now, using the RFM model, the customer segmentation is done!

Translating RFM Scores to Segments Sources: 
- https://connectif.ai/en/blog/what-are-rfm-scores-and-how-to-calculate-them/
- https://www.linkedin.com/pulse/rfm-customer-segmentation-analysis-action-jason-tragakis-0ffrf/
