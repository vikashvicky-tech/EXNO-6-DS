# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

x = [1, 2, 3, 4, 5]

y = [3, 6, 2, 7, 1]

sns.lineplot(x=x,y=y)

<img width="827" height="578" alt="Screenshot 2025-10-10 131142" src="https://github.com/user-attachments/assets/984ab8c4-e949-4963-a368-b40ced1d2cd4" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

df = sns.load_dataset("tips")

df

<img width="649" height="457" alt="Screenshot 2025-10-10 131247" src="https://github.com/user-attachments/assets/f2c29ef0-9c4c-4104-ae8a-0796a3aa1049" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")

<img width="855" height="589" alt="Screenshot 2025-10-10 131320" src="https://github.com/user-attachments/assets/440968c4-b615-45bd-94d5-ffbfdc86bcd2" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

x=[1, 2, 3, 4, 5]

y1=[3, 5, 2, 6, 1]

y2=[1, 6, 4, 3, 8]

y3=[5, 2, 7, 1, 4]

sns.lineplot(x=x, y=y1)

sns.lineplot(x=x, y=y2)

sns.lineplot(x=x, y=y3)

plt.title("Multi-Line Plot")

plt.xlabel('X Label')

plt.ylabel("Y Label")

<img width="894" height="637" alt="Screenshot 2025-10-10 131415" src="https://github.com/user-attachments/assets/8a4978cc-375a-41b3-a168-9102e7637ff7" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tips=sns.load_dataset('tips')

avg_total_bill = tips.groupby('day')['total_bill'].mean()

avg_tip = tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8, 6))

p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')

p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')

plt.xlabel('Day of the Week')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Day')

plt.legend()

<img width="1045" height="722" alt="Screenshot 2025-10-10 131513" src="https://github.com/user-attachments/assets/a5f74d7a-af7f-4858-99e4-4ffd391e03c0" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

avg_total_bill = tips.groupby('time')['total_bill'].mean()

avg_tip=tips.groupby('time') ['tip'].mean()

p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)

p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)

<img width="729" height="552" alt="Screenshot 2025-10-10 131547" src="https://github.com/user-attachments/assets/841ca658-e44f-4497-ad0c-679550f718a5" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

years=range(2000, 2012)

apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]

oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]

plt.bar(years, apples)

plt.bar(years, oranges, bottom=apples)

<img width="871" height="579" alt="Screenshot 2025-10-10 131633" src="https://github.com/user-attachments/assets/65a545ad-156a-404f-9cd8-70b60cad096d" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

dt= sns.load_dataset('tips')

sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')

plt.xlabel('Day of the Week')

plt.ylabel("Total Bill")

plt.title('Total Bill by Day and Gender')

<img width="849" height="610" alt="Screenshot 2025-10-10 131714" src="https://github.com/user-attachments/assets/a45f19a8-4570-49cf-9180-4869bf4e1f81" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tit=pd.read_csv("titanic_dataset.csv")

tit

<img width="1362" height="468" alt="Screenshot 2025-10-10 131836" src="https://github.com/user-attachments/assets/8afa0a71-6572-41c8-82b4-f01da6d4a5e6" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')

plt.title("Fare of Passenger by Embarked Town")

<img width="1051" height="650" alt="Screenshot 2025-10-10 131918" src="https://github.com/user-attachments/assets/b729a38f-9090-4ec6-bb58-aa95a86cd50a" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')

plt.title("Fare of Passenger by Embarked Town, Divided by Class")

<img width="1065" height="641" alt="Screenshot 2025-10-10 131955" src="https://github.com/user-attachments/assets/186c225b-ee55-4fdd-a483-435ccc15bd83" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tips=sns.load_dataset('tips')

sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)

plt.xlabel('Total Bill')

plt.ylabel("Tip Amount")

plt.title('Scatter Plot of Total Bill vs. Tip Amount')

<img width="859" height="637" alt="Screenshot 2025-10-10 132037" src="https://github.com/user-attachments/assets/10edef20-6284-4edd-a5c9-165cf97f8505" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

num_var = np.random.randn(1000)

num_var=pd.Series(num_var, name = "Numerical variable")

num_var

<img width="682" height="285" alt="Screenshot 2025-10-10 132110" src="https://github.com/user-attachments/assets/7e82551f-763f-4941-817b-64c4080b0817" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.histplot(data = num_var, kde = True)

<img width="881" height="598" alt="Screenshot 2025-10-10 132158" src="https://github.com/user-attachments/assets/8a91b951-aedc-486c-b41d-271d3aa2ddbc" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

df=pd.read_csv("titanic_dataset.csv")

sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)

<img width="908" height="588" alt="Screenshot 2025-10-10 132237" src="https://github.com/user-attachments/assets/e7527e9f-b261-4886-8f47-3c9ee013106d" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tips=sns.load_dataset('tips')

sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])

<img width="917" height="585" alt="Screenshot 2025-10-10 132317" src="https://github.com/user-attachments/assets/07e23616-5523-4acd-a873-5851fe44584e" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})

<img width="883" height="592" alt="Screenshot 2025-10-10 132400" src="https://github.com/user-attachments/assets/751ea323-7846-4052-add8-f0d53eaf96c2" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")

plt.xlabel("Day of the Week")

plt.ylabel("Total Bill")

plt.title("Violin Plot of Total Bill by Day and Smoker Status")

<img width="843" height="628" alt="Screenshot 2025-10-10 132458" src="https://github.com/user-attachments/assets/359e5671-940a-4c64-a068-58aa0ab5ef98" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

mart=pd.read_csv("titanic_dataset.csv")

mart

<img width="1365" height="429" alt="Screenshot 2025-10-10 132539" src="https://github.com/user-attachments/assets/d0ecf83b-6002-495a-8642-1da90f094cf8" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]

mart.head(10)

<img width="984" height="380" alt="Screenshot 2025-10-10 132619" src="https://github.com/user-attachments/assets/afcb2a09-8d73-4ceb-8f36-d44312df45fc" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart,x='PassengerId')

<img width="952" height="588" alt="Screenshot 2025-10-10 132649" src="https://github.com/user-attachments/assets/b8eb763f-c911-4348-af3c-2f07a9f2f36d" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart,x='Age')

<img width="915" height="608" alt="Screenshot 2025-10-10 132724" src="https://github.com/user-attachments/assets/c74dcb40-2992-4da3-9114-9a84df2680da" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart)

<img width="921" height="600" alt="Screenshot 2025-10-10 132814" src="https://github.com/user-attachments/assets/48eb3736-75f3-4eb3-a16f-100942c0e9ec" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')

<img width="910" height="600" alt="Screenshot 2025-10-10 132848" src="https://github.com/user-attachments/assets/c57c54e4-0519-4775-8c75-36a22ad80b4e" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart,x='PassengerId',y='Survived')

<img width="976" height="579" alt="Screenshot 2025-10-10 132933" src="https://github.com/user-attachments/assets/67dd21e2-d610-4c0a-87da-c3566301109a" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

data = np.random.randint(low = 1, high = 100, size = (10,10))

hm=sns.heatmap(data=data,annot=True)

<img width="692" height="555" alt="Screenshot 2025-10-10 133008" src="https://github.com/user-attachments/assets/632ddbde-453b-4c72-8d66-45366d1117b5" />

# Result:
 Thus data visualisation using seaborn python library is performed.
