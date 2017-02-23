# HKEX_Stakeholder_Change_List
List the Changes of HKEX Stakeholders with >5% stakes

# source:
# Search by Date : 23/02/2016&sced=23/02/2017&
#http://sdinotice.hkex.com.hk/di/NSAllFormDateList.aspx?sa1=da&scsd=23/02/2016&sced=23/02/2017&src=MAIN&lang=ZH

This is a very basic HTML Table Parser that aims at parsing the changes of stakeholders and their stakes in different stocks on the Hong Kong stock market.

I've overcome a few issues during the development:
*****************************
(1) Encoding issue
Since the website of Hong Kong Stock Exchange is partly Chinese, developing the Table Parser in Windows is a headache as there was an encoding/decoding issue.

Solution: Add "encoding='utf-8-sig'" to the open instruction

with open('names.csv', 'a', encoding='utf-8-sig') as csvfile:
        writer = csv.writer(csvfile)
        writer.writerow(['Date', 'Corporation', 'Shareholder', 'Code', 'Shares Involved', 'Average Price', 'Total Shares', '% of issued shared'])
*****************************


*****************************
(2) Lack of proper use of functions
I'm a beginner in Python, so I decided to make a product first, and improve it later.

I'm aware that I could have used more functions to have the job done. But confidence is what a beginner needs lol
*****************************
