
<a href="https://nbviewer.jupyter.org/github/reyvaz/Mining-Medical-Records/blob/master/dates.ipynb" target="_blank">Click Here</a>
to see the Notebook online in Jupyter nbviewer.

## Data Mining: Extracting Dates from Messy Medical Records

Extracts dates from messy medical notes using regular expressions on Pandas

Each data instance corresponds to a medical note containing a date written in one of many formats.

Examples of date encoding variants in the data are: 

* 03/20/2009; 03/20/09; 3-20-09  
* Mar-20-2009; Mar 20, 2009; March 20, 2009;  Mar. 20, 2009; Mar 20 2009  
* 20 Mar 2009; 20 March 2009; 20 Mar. 2009; 20 March, 2009  
* 3/09, 2009  

Including some typos and other confounding errors/formats. 


### Sample of original data

```
171                                              04 Oct 1972 Total time of visit (in minutes):\n
72     Lithium 0.25 (7/11/77).  LFTS wnl.  Urine tox neg.  Serum tox + fluoxetine 500; otherw...
378    The pt. is a 45 Y/O F who comes in to discuss her sexual problems-low libido.  Factors...
24                                             07/25/1984 CPT Code: 90791: No medical services\n
455                                        sHemmorage caused by probe in 1984 Medical History:\n
269            passive SI only (most recent episode end of July 1992) If Yes, please describe:\n
2                                       sshe plans to move as of 7/8/71 In-Home Services: None\n
159    .The patient brought himself to APS on 26 May 2001 for ONE MONTH HISTORY of recurrence...
177    22 year old single Caucasian/Latino woman, unemployed Cook recent college graduate, li...
175     .On 21 Oct 1983 patient was discharged from Scroder Hospital after EIGHT DAY ADMISSION\n
dtype: object
```
### Sample output dates
```
171   1972-10-04
72    1977-07-11
378   1978-12-01
24    1984-07-25
455   1984-01-01
269   1992-07-01
2     1971-07-08
159   2001-05-26
177   1990-01-18
175   1983-10-21
```

