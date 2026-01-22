# Histogram-vs-Bar-Plot

Python Histogram

a. Simple Example

import seaborn as sn

import matplotlib.pyplot as plt

df = sn.load_dataset('planets')

sn.histplot(df['year'], kde=True)

plt.title('Discovery Year of Exoplanets')

Text(0.5, 1.0, 'Discovery Year of Exoplanets')

plt.show()

<img width="640" height="480" alt="example histogram garis lengkung" src="https://github.com/user-attachments/assets/60d5e15a-3b24-46ac-bf1a-1c1110d54a64" />

import numpy as np

import matplotlib.pyplot as plt

np.random.seed(42)

N = 100000

n_bins = 30

x = 50 + 15 * np.random.randn(N)

y = 80 + 5 * np.random.randn(N)

fig, axs = plt.subplots(1, 2, sharey=True, tight_layout=True, figsize=(10, 5))

axs[0].hist(x, bins=n_bins, color='#2ecc71', edgecolor='white')

axs[0].set_title('Productivity Scores (Group A)')

axs[1].hist(y, bins=n_bins, color='#3498db', edgecolor='white')

axs[1].set_title('Productivity Scores (Group B)')

plt.show()

<img width="1000" height="500" alt="example histogram 2" src="https://github.com/user-attachments/assets/c253f6db-5473-40f6-9f3c-5a1847b6b9f9" />

b. Displaying Only The Histogram

import seaborn as sn

import matplotlib.pyplot as plt

df = sn.load_dataset('planets')

sn.histplot(df['year'])

plt.title('Discovery Year of Exoplanets')

plt.show()

<img width="640" height="480" alt="example histogram" src="https://github.com/user-attachments/assets/3f16dcbc-dd68-419d-9844-5130e2c0aa43" />

c. Displaying Histogram, Rug, and Kernel Density

import seaborn as sn

import matplotlib.pyplot as plt

df = sn.load_dataset('planets')

sn.histplot(df['year'], kde=True)

sn.rugplot(df['year'])

plt.show()

<img width="640" height="480" alt="example histogram kde, rug" src="https://github.com/user-attachments/assets/488509ef-2c1e-42bb-b88e-966ac23248f6" />

d. Customizing the rug

import seaborn as sn

import matplotlib.pyplot as plt

df = sn.load_dataset('planets')

sn.histplot(df['year'], kde=True)

sn.rugplot(df['year'], color='r', alpha=0.35, linewidth=5)

plt.title('Discovery Year of Exoplanets')

Text(0.5, 1.0, 'Discovery Year of Exoplanets')

plt.show()

<img width="640" height="480" alt="example histogram custom rug" src="https://github.com/user-attachments/assets/1798a033-7722-4787-8cdb-fc4b33c5941b" />

e. Vertical Python Histogram

import seaborn as sn

import matplotlib.pyplot as plt

df = sn.load_dataset('planets')

sn.histplot(y=df['year'], kde=True, color='lavender')

plt.title('Discovery Year of Exoplanets (Vertical)')

Text(0.5, 1.0, 'Discovery Year of Exoplanets (Vertical)')

plt.show()

<img width="640" height="480" alt="example histogram vertical" src="https://github.com/user-attachments/assets/a2517d5c-56f8-48e1-bad7-cd20f9b695f8" />

f. Python Histogram with multiple variables

import seaborn as sn

import matplotlib.pyplot as plt

df = sn.load_dataset('planets')

sn.histplot(df['year'], kde=True, color='yellow', label='Year')

sn.histplot(df['distance'].dropna(), kde=True, color='green', label='Distance')

plt.legend()

plt.title('Comparison: Discovery Year vs Distance of Planets')

Text(0.5, 1.0, 'Comparison: Discovery Year vs Distance of Planets')

plt.show()

<img width="640" height="480" alt="example histogram multiple variables" src="https://github.com/user-attachments/assets/4ccbea4a-10c1-4a53-934e-eb2351f27d5a" />



Python Bar Plot

a. Example

import numpy as np

import matplotlib.pyplot as plt

marks=[67,55,32,79,85]

bars=('Tahu','Tempe','Nugget','Gehu','Risol')

y=np.arange(len(bars))

plt.bar(y, marks, color='b')

plt.xticks(y,bars)

plt.show()

<img width="640" height="480" alt="example bar plot" src="https://github.com/user-attachments/assets/77ca9f32-98b1-4e2d-8add-5d1182a628c5" />

b. Setting a Different Color for Each Bar

import numpy as np

import matplotlib.pyplot as plt

marks=[67,55,32,79,85]

bars=('Tahu','Tempe','Nugget','Gehu','Risol')

y=np.arange(len(bars))

plt.bar(y, marks, color=['#FFB7B2', '#FFDAC1', '#E2F0CB', '#B5EAD7', '#C7CEEA'])

plt.xticks(y,bars)

plt.show()

<img width="640" height="480" alt="example bar plot sett diff color" src="https://github.com/user-attachments/assets/f60418f5-343c-4143-88c8-ad24c803dc06" />

c. Setting Border Color

import numpy as np

import matplotlib.pyplot as plt

marks=[67,55,32,79,85]

bars=('Tahu','Tempe','Nugget','Gehu','Risol')

y=np.arange(len(bars))

plt.bar(y,marks,color=(0.2,0.4,0.2,0.7),edgecolor='yellow')

plt.xticks(y,bars)

plt.show()

<img width="640" height="480" alt="setting border color" src="https://github.com/user-attachments/assets/cf74ffbb-bbe6-484c-b125-948f845fa173" />

d. Horizontal Python Bar Plot

import numpy as np

import matplotlib.pyplot as plt

marks = [67, 55, 32, 79, 85]

bars = ('Tahu', 'Tempe', 'Nugget', 'Gehu', 'Risol')

y = np.arange(len(bars))

warna_pastel = ['#FFB7B2', '#FFDAC1', '#E2F0CB', '#B5EAD7', '#C7CEEA']

plt.barh(y, marks, color=warna_pastel)

plt.yticks(y, bars)

plt.show()

<img width="640" height="480" alt="example bar plot horizontal" src="https://github.com/user-attachments/assets/d5e28941-d239-4812-a721-89d2e237fbf8" />


