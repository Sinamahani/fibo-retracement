import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_excel(r'C:\Users\mehdi\Downloads\Gold Futures Historical Data.xlsx')
df = df.set_index('Date',drop = False)

Price_Min =df['Low'].min()
Price_Max =df['High'].max()

Diff = Price_Max-Price_Min

level1 = Price_Max - 0.236 * Diff
level2 = Price_Max - 0.382 * Diff
level3 = Price_Max - 0.5   * Diff
level4 = Price_Max - 0.618 * Diff
level5 = Price_Max - 0.707 * Diff



fig, ax = plt.subplots(figsize=(15,5))

ax.plot(df.Date, df.Price)

ax.axhspan(level1, Price_Min, alpha=0.4, color='rosybrown')
ax.axhspan(level2, level1, alpha=0.5, color='goldenrod')
ax.axhspan(level3, level2, alpha=0.5, color='azure')
ax.axhspan(level4, level3, alpha=0.5, color='ivory')
ax.axhspan(level5, level4, alpha=0.5, color='palegreen')
ax.axhspan(Price_Max, level3, alpha=0.5, color='lightskyblue')

plt.ylabel("Price")
plt.xlabel("Date")

plt.title('Fibonacci')

plt.show()

print ("Level", " ", "PRICE")
print ("0 ", "      " , Price_Max)
print ("0.236", "   " ,level1)
print ("0.382",  "   ",level2)
print ("0.618","   ",  level3)
print ("1 ",   "      ", Price_Min)
