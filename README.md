# RIS-to-CSV
#first import csv, defaultdict, rispy and pandas as given here:

     import csv
     from collections import defaultdict
     import pandas as pd
     from rispy import load

#then open by function with open, choose your file path in tt2.ris for example your ris file path.

        with open("tt2.ris", "r", encoding="utf-8") as f:
         entries = list(load(f))
         df =pd.DataFrame(entries)
 #put your outfile path in "csv file3"
 
         df.to_csv("csv file3.csv", index=False)
        print("Ris converted to csv using pandas")
 #ris converted to csv using pandas
