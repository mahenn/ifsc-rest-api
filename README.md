# Rest API to get details of  NEFT enabled bank Branches (Bank-wise IFS Codes).
> Note: All details are taken from  [RBI website](https://www.rbi.org.in/Scripts/bs_viewcontent.aspx?Id=2009) last update Jan 22, 2016.

###Features provided 

 1. Get supported bank list
 2. Get bank by IFSC code.
 3. Get bank by MICR code.
 4. Get banks by bank name.
 5. Get banks by branch location.
 6. Get banks by district
 7. Get banks by state


##API Documentation


### Get supported bank list

####URI : `http://api.techm.co.in/api/listbanks`

Example:
 http://api.techm.co.in/api/listbanks

Sample response:


   {"status": "success", "data":["ABU DHABI COMMERCIAL BANK","ABHYUDAYA COOPERATIVE BANK LIMITED", .............]}


 ###Get bank by IFSC code.

####URI : `http://api.techm.co.in/api/ifsc/{IFSC CODE}`
Request Type: GET

Example:
 http://api.techm.co.in/api/ifsc/SBIN0000138
Sample response:

    [{
    	"_id": "56a4e61d277fdd0a3417ebbb",
    	"STATE": "BIHAR",
    	"BANK": "STATE BANK OF INDIA",
    	"IFSC": "SBIN0000138",
    	"MICR CODE": "842002002",
    	"BRANCH": "MUZAFFARPUR",
    	"CONTACT": "0",
    	"ADDRESS": "MUZAFFARPUR, BIHAR, PIN 842001",
    	"CITY": "MUZAFFARPUR",
    	"DISTRICT": "MUZAFFARPUR"
    }]
###Get bank by MICR code

####URI : `http://api.techm.co.in/api/micr/{MICR CODE}`
Request Type: GET

Example: 
http://api.techm.co.in/api/micr/842002002

    [{
    	"_id": "56a4e61d277fdd0a3417ebbb",
    	"STATE": "BIHAR",
    	"BANK": "STATE BANK OF INDIA",
    	"IFSC": "SBIN0000138",
    	"MICR CODE": "842002002",
    	"BRANCH": "MUZAFFARPUR",
    	"CONTACT": "0",
    	"ADDRESS": "MUZAFFARPUR, BIHAR, PIN 842001",
    	"CITY": "MUZAFFARPUR",
    	"DISTRICT": "MUZAFFARPUR"
    }]

###Get banks by bank name

####URI : `http://api.techm.co.in/api/bank/{Bank NAME}`

Request Type: GET

Example:
http://api.techm.co.in/api/bank/ABU%20DHABI%20COMMERCIAL%20BANK
Sample response:

    [{
    	"_id": "56a4e606277fdd0a341698cb",
    	"STATE": "MAHARASHTRA",
    	"BANK": "ABU DHABI COMMERCIAL BANK",
    	"IFSC": "ADCB0000001",
    	"MICR CODE": "400269002",
    	"BRANCH": "RTGS-HO",
    	"CONTACT": "39534100",
    	"ADDRESS": "75, REHMAT MANZIL, V. N. ROAD, CURCHGATE, MUMBAI - 400020",
    	"CITY": "MUMBAI",
    	"DISTRICT": "MUMBAI CITY"
    }, {
    	"_id": "56a4e606277fdd0a341698cc",
    	"STATE": "KARNATAKA",
    	"BANK": "ABU DHABI COMMERCIAL BANK",
    	"IFSC": "ADCB0000002",
    	"MICR CODE": "560269002",
    	"BRANCH": "BANGALORE",
    	"CONTACT": "25582000",
    	"ADDRESS": "CITI CENTRE, 28, CHURCH STREET, OFF M. G. ROAD BANGALORE 560001",
    	"CITY": "BANGALORE",
    	"DISTRICT": "BANGALORE URBAN"
    }]
    
####Get banks by branch location
URI : `http://api.techm.co.in/api/branch/{BRANCH NAM`E}
Request type: GET

Example:
http://api.techm.co.in/api/branch/KASHMIR

    [{
    	"_id": "56a4e624277fdd0a34186909",
    	"": "",
    	"BANK": "UCO BANK",
    	"IFSC": "UCBA0001539",
    	"MICR CODE": "177028054",
    	"BRANCH": "KASHMIR",
    	"CONTACT": "239021",
    	"ADDRESS": "R V & PO KASHMIRDISTT-HAMIRPUR 177006",
    	"CITY": "KASHNIUR",
    	"DISTRICT": "HAMIRPUR",
    	"STATE": "HIMACHAL PRADESH"
    }]

###Get bank list by district name

####URI : `http://api.techm.co.in/api/district/{district name}`

Request Type: GET

Example:
http://api.techm.co.in/api/district/mumbai
http://api.techm.co.in/api/district/patna

Sample Response:

    {"status":"success","data":[{"_id":"56e022edd632a3912074e793","STATE":"GOA","BANK":"ALLAHABAD BANK","IFSC":"ALLA0210994","MICR CODE":"403010003","BRANCH":"MAPUCA","CONTACT":"2262801","ADDRESS":"HOTEL SATYA HEERA BUILDING, NEAR HANUMAN TEMPLE, MAPUSA, NORTHGOA 403507","CITY":"MAPUSA","DISTRICT":"NORTH GOA"}]}

###Get bank list by state name

####URI : `http://api.techm.co.in/api/state/{state name}`

Request Type: GET

Example:
http://api.techm.co.in/api/state/goa
http://api.techm.co.in/api/state/Uttar%20pradesh

Sample Response:

    {"status":"success","data":[{"_id":"56e022edd632a3912074e793","STATE":"GOA","BANK":"ALLAHABAD BANK","IFSC":"ALLA0210994","MICR CODE":"403010003","BRANCH":"MAPUCA","CONTACT":"2262801","ADDRESS":"HOTEL SATYA HEERA BUILDING, NEAR HANUMAN TEMPLE, MAPUSA, NORTHGOA 403507","CITY":"MAPUSA","DISTRICT":"NORTH GOA"}]}



###We provide details of following banks:

1. ABHYUDAYA COOPERATIVE BANK LIMITED
2. ABU DHABI COMMERCIAL BANK
3. AHMEDABAD MERCANTILE COOPERATIVE BANK
4. AKOLA JANATA COMMERCIAL COOPERATIVE BANK
5. ALLAHABAD BANK
6. ALMORA URBAN COOPERATIVE BANK LIMITED
7. ANDHRA BANK
8. ANDHRA PRAGATHI GRAMEENA BANK
9. APNA SAHAKARI BANK LIMITED
10. AUSTRALIA AND NEW ZEALAND BANKING GROUP LIMITED
11. AXIS BANK
12. B N P PARIBAS
13. BANDHAN BANK LIMITED
14. BANK INTERNASIONAL INDONESIA
15. BANK OF AMERICA
16. BANK OF BAHARAIN AND KUWAIT BSC
17. BANK OF BARODA
18. BANK OF CEYLON
19. BANK OF INDIA
20. BANK OF MAHARASHTRA
21. BANK OF TOKYO MITSUBISHI LIMITED
22. BARCLAYS BANK
23. BASSEIN CATHOLIC COOPERATIVE BANK LIMITED
24. BHARAT COOPERATIVE BANK MUMBAI LIMITED
25. BHARATIYA MAHILA BANK LIMITED
26. CANARA BANK
27. CAPITAL LOCAL AREA BANK LIMITED
28. CATHOLIC SYRIAN BANK LIMITED
29. CENTRAL BANK OF INDIA
30. CHINATRUST COMMERCIAL BANK LIMITED
31. CITI BANK
32. CITIZEN CREDIT COOPERATIVE BANK LIMITED
33. CITY UNION BANK LIMITED
34. COMMONWEALTH BANK OF AUSTRALIA
35. CORPORATION BANK
36. CREDIT AGRICOLE CORPORATE AND INVESTMENT BANK CALYON BANK
37. CREDIT SUISEE AG
38. DCB BANK LIMITED
39. DENA BANK
40. DEPOSIT INSURANCE AND CREDIT GUARANTEE CORPORATION
41. DEUSTCHE BANK
42. DEVELOPMENT BANK OF SINGAPORE
43. DHANALAKSHMI BANK
44. DOHA BANK
45. DOHA BANK QSC
46. DOMBIVLI NAGARI SAHAKARI BANK LIMITED
47. EXPORT IMPORT BANK OF INDIA
48. FEDERAL BANK
49. FIRSTRAND BANK LIMITED
50. G P PARSIK BANK
51. GURGAON GRAMIN BANK
52. HDFC BANK
53. HSBC BANK
54. HSBC BANK OMAN SAOG
55. ICICI BANK LIMITED
56. IDBI BANK
57. IDFC BANK LIMITED
58. INDIAN BANK
59. INDIAN OVERSEAS BANK
60. INDUSIND BANK
61. INDUSTRIAL AND COMMERCIAL BANK OF CHINA LIMITED
62. INDUSTRIAL BANK OF KOREA
63. ING VYSYA BANK
64. JALGAON JANATA SAHAKARI BANK LIMITED
65. JAMMU AND KASHMIR BANK LIMITED
66. JANAKALYAN SAHAKARI BANK LIMITED
67. JANASEVA SAHAKARI BANK BORIVLI LIMITED
68. JANASEVA SAHAKARI BANK LIMITED
69. JANATA SAHAKARI BANK LIMITED
70. JP MORGAN BANK
71. KALLAPPANNA AWADE ICHALKARANJI JANATA SAHAKARI BANK LIMITED
72. KALUPUR COMMERCIAL COOPERATIVE BANK
73. KALYAN JANATA SAHAKARI BANK
74. KAPOL COOPERATIVE BANK LIMITED
75. KARNATAKA BANK LIMITED
76. KARNATAKA VIKAS GRAMEENA BANK
77. KARUR VYSYA BANK
78. KERALA GRAMIN BANK
79. KOTAK MAHINDRA BANK LIMITED
80. LAXMI VILAS BANK
81. MAHANAGAR COOPERATIVE BANK
82. MAHARASHTRA STATE COOPERATIVE BANK
83. MASHREQBANK PSC
84. MIZUHO CORPORATE BANK LIMITED
85. NAGAR URBAN CO OPERATIVE BANK
86. NAGPUR NAGARIK SAHAKARI BANK LIMITED
87. NATIONAL AUSTRALIA BANK LIMITED
88. NATIONAL BANK OF ABU DHABI PJSC
89. NEW INDIA COOPERATIVE BANK LIMITED
90. NKGSB COOPERATIVE BANK LIMITED
91. NUTAN NAGARIK SAHAKARI BANK LIMITED
92. OMAN INTERNATIONAL BANK SAOG
93. ORIENTAL BANK OF COMMERCE
94. PRAGATHI KRISHNA GRAMIN BANK
95. PRATHAMA BANK
96. PRIME COOPERATIVE BANK LIMITED
97. PUNJAB AND MAHARSHTRA COOPERATIVE BANK
98. PUNJAB AND SIND BANK
99. PUNJAB NATIONAL BANK
100. RABOBANK INTERNATIONAL
101. RAJGURUNAGAR SAHAKARI BANK LIMITED
102. RAJKOT NAGRIK SAHAKARI BANK LIMITED
103. RBL BANK LIMITED
104. RESERVE BANK OF INDIA
105. SAHEBRAO DESHMUKH COOPERATIVE BANK LIMITED
106. SARASWAT COOPERATIVE BANK LIMITED
107. SBER BANK
108. SBM BANK MAURITIUS LIMITED
109. SHIKSHAK SAHAKARI BANK LIMITED
110. SHINHAN BANK
111. SHRI CHHATRAPATI RAJASHRI SHAHU URBAN COOPERATIVE BANK LIMITED
112. SOCIETE GENERALE
113. SOLAPUR JANATA SAHAKARI BANK LIMITED
114. SOUTH INDIAN BANK
115. STANDARD CHARTERED BANK
116. STATE BANK OF BIKANER AND JAIPUR
117. STATE BANK OF HYDERABAD
118. STATE BANK OF INDIA
119. STATE BANK OF MAURITIUS LIMITED
120. STATE BANK OF MYSORE
121. STATE BANK OF PATIALA
122. STATE BANK OF TRAVANCORE
123. SUMITOMO MITSUI BANKING CORPORATION
124. SURAT NATIONAL COOPERATIVE BANK LIMITED
125. SUTEX COOPERATIVE BANK LIMITED
126. SYNDICATE BANK
127. TAMILNAD MERCANTILE BANK LIMITED
128. THE A.P. MAHESH COOPERATIVE URBAN BANK LIMITED
129. THE AKOLA DISTRICT CENTRAL COOPERATIVE BANK
130. THE ANDHRA PRADESH STATE COOPERATIVE BANK LIMITED
131. THE BANK OF NOVA SCOTIA
132. THE COSMOS CO OPERATIVE BANK LIMITED
133. THE DELHI STATE COOPERATIVE BANK LIMITED
134. THE GADCHIROLI DISTRICT CENTRAL COOPERATIVE BANK LIMITED
135. THE GREATER BOMBAY COOPERATIVE BANK LIMITED
136. THE GUJARAT STATE COOPERATIVE BANK LIMITED
137. THE HASTI COOP BANK LTD
138. THE JALGAON PEOPELS COOPERATIVE BANK LIMITED
139. THE KANGRA CENTRAL COOPERATIVE BANK LIMITED
140. THE KANGRA COOPERATIVE BANK LIMITED
141. THE KARAD URBAN COOPERATIVE BANK LIMITED
142. THE KARANATAKA STATE COOPERATIVE APEX BANK LIMITED
143. THE KURMANCHAL NAGAR SAHAKARI BANK LIMITED
144. THE MEHSANA URBAN COOPERATIVE BANK
145. THE MUMBAI DISTRICT CENTRAL COOPERATIVE BANK LIMITED
146. THE MUNICIPAL COOPERATIVE BANK LIMITED
147. THE NAINITAL BANK LIMITED
148. THE NASIK MERCHANTS COOPERATIVE BANK LIMITED
149. THE RAJASTHAN STATE COOPERATIVE BANK LIMITED
150. THE ROYAL BANK OF SCOTLAND N V
151. THE SEVA VIKAS COOPERATIVE BANK LIMITED
152. THE SHAMRAO VITHAL COOPERATIVE BANK
153. THE SURAT DISTRICT COOPERATIVE BANK LIMITED
154. THE SURATH PEOPLES COOPERATIVE BANK LIMITED
155. THE TAMIL NADU STATE APEX COOPERATIVE BANK
156. THE THANE BHARAT SAHAKARI BANK LIMITED
157. THE THANE DISTRICT CENTRAL COOPERATIVE BANK LIMITED
158. THE VARACHHA COOPERATIVE BANK LIMITED
159. THE VISHWESHWAR SAHAKARI BANK LIMITED
160. THE WEST BENGAL STATE COOPERATIVE BANK
161. THE ZOROASTRIAN COOPERATIVE BANK LIMITED
162. TJSB SAHAKARI BANK LIMITED
163. TJSB SAHAKARI BANK LTD
164. TUMKUR GRAIN MERCHANTS COOPERATIVE BANK LIMITED
165. UCO BANK
166. UNION BANK OF INDIA
167. UNITED BANK OF INDIA
168. UNITED OVERSEAS BANK LIMITED
169. VASAI VIKAS SAHAKARI BANK LIMITED
170. VIJAYA BANK
171. WESTPAC BANKING CORPORATION
172. WOORI BANK
173. YES BANK
174. ZILA SAHAKRI BANK LIMITED GHAZIABAD

