# e-energy
Sudo Code : 
https://dl.acm.org/citation.cfm?id=3208941

## Experimental settings
<br />
The time slot for DR events is one hour. The maximum number of requests that can be sent to a consumer for the period is 5, after which the consumer is filtered out from the selection process. We define a flat supply threshold across all time slots, where AG equals to 90% of the maximum demand on the DR day. Expected reduction for every consumer is 40 percent of their total consumption. Initially, ∆t is assigned zero and is updated in the subsequent iterations based on the responses in the previous iteration. The response index and request index are created using a random function, that takes values between 0.1 and 0.9 respectively. Experiments are run in a Stochastic Response Mode for 10 DR events. 
Each time a consumer gets selected, it's requesting index and response index are updated using equation 5 and equation 6. Consumer's expected reduction for every DR event is calculated using a function based on their average performance in the past DR events ±a % randomly, where takes values from 1 to 10, multiplied by 0.4.
Experiments For evaluation, all possible combinations, i.e.,4C1,4C2,4C3 and 4C4 of features are considered. For simplicity, while calculating the overall score, all features under consideration are given the same alpha values, i.e., 1 and rest to 0. All these combinations result in in 15 different approaches. The performance metrics  are measured for all these approaches using equations 10, 12, 13 mentioned in the paper. Maximum possible value for T(Number of DR requests) is 5000 which occurs when DR Request is sent to every consumer in all DR events. The maximum risk which can be obtained is 100% and worst case unfairness will be close to 500
<br />
<br />


## Dataset
The dataset consists of electricity consumption data (December 2016 to June 2018) from a high-rise residential building inside the IIT Bombay campus. The building consists of 60 3BHK(3 Bedrooms, I Hall and a Kitchen) apartments, each instrumented with a smart-meter, logging data at a sampling period of 5s. The data shared in the link below is downsampled at 1-hour granularity. All the timestamps mentioned in the dataset is of Indian Standard Time(GMT+5.30), and India doesn’t follow daylight saving time. For privacy reasons, apartments are kept anonymous. The folder consists of 39 CSV files each representing an apartment. Apartments having significant data loss are removed from the list. The headers in the CSV files are as follows:
<br />
<br />

1)TS – Unix Time stamp (epochs)<br />
2)V1 – Voltage of phase 1 (V)<br />
3)V2 – Voltage of phase 2  (V)<br />
4)V3 – Voltage of phase 3  (V)<br />
5)W1 – Electricity consumption of phase 1 (Wh)<br />
6)W2 – Electricity consumption of phase 2 (Wh)<br />
7)W3 – Electricity consumption of phase 3 (Wh)<br />


## Virtual Dataset
<br />
Additional Headers<br />

8)Virtual Apartment- VirtualApartment ID<br />
9)Date – Date in YYYY-MM-DD<br />
10)Time – Time in HH:MM:SS<br />
11)Energy- Sum of W1 + W2 + W3 (Wh)<br />

<br />
Link for the dataset http://seil.cse.iitb.ac.in/residential-dataset/
<br />
Please use the following BibTex to cite the dataset<br />
<br />

@inproceedings{mammen2018want,
title={Want to Reduce Energy Consumption, Whom should we call?},
author={Mammen, Priyanka Mary and Kumar, Hareesh and Ramamritham, Krithi and Rashid, Haroon},
booktitle={Proceedings of the Ninth International Conference on Future Energy Systems},
pages={12–20},
year={2018},
organization={ACM}
}

<br/>
 
## Issues
If you face any issues with the dataset, please feel free to reach us at seil@cse.iitb.ac.in.
<br />

To contact authors:<br />
Priyanka Mary Mammen : priyankam@cse.iitb.ac.in<br />
Hareesh Kumar : hareesh@iitb.ac.in<br />
Krithi Ramamritham : krithi@iitb.ac.in<br />
Haroon Rashid : haroonr@iiitd.ac.in<br />

Creative Commons License<br />
This work is licensed under a Creative Commons Attribution 4.0 International License.<br />
