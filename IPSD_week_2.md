#Nama Anggota

##1. Alvia Bunga Patricia , 103102400072
##2. Muhammad Daffa Wardana , 103102400004
##3. Alfalaq Axcellio Gais Blantra , 103102400075
##4. Nisrina Hibatullah , 103102400013
##5. Hasna Maritsa, 103102400059

##1.Load Data ##

Memasukkan dataset Disney Plus Shows ke Python menggunakan pandas



```python
import pandas as pd
import matplotlib.pyplot as plt
import matplotlib

df = pd.read_csv('/content/disney_plus_shows.csv')
display(df.head())
```



  <div id="df-51c77191-6297-4a12-9543-1f00e29c3095" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>imdb_id</th>
      <th>title</th>
      <th>plot</th>
      <th>type</th>
      <th>rated</th>
      <th>year</th>
      <th>released_at</th>
      <th>added_at</th>
      <th>runtime</th>
      <th>genre</th>
      <th>director</th>
      <th>writer</th>
      <th>actors</th>
      <th>language</th>
      <th>country</th>
      <th>awards</th>
      <th>metascore</th>
      <th>imdb_rating</th>
      <th>imdb_votes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0147800</td>
      <td>10 Things I Hate About You</td>
      <td>A pretty, popular teenager can't go out on a d...</td>
      <td>movie</td>
      <td>PG-13</td>
      <td>1999</td>
      <td>31 Mar 1999</td>
      <td>November 12, 2019</td>
      <td>97 min</td>
      <td>Comedy, Drama, Romance</td>
      <td>Gil Junger</td>
      <td>Karen McCullah, Kirsten Smith</td>
      <td>Heath Ledger, Julia Stiles, Joseph Gordon-Levi...</td>
      <td>English, French</td>
      <td>USA</td>
      <td>2 wins &amp; 13 nominations.</td>
      <td>70.0</td>
      <td>7.3</td>
      <td>283,945</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt7019028</td>
      <td>101 Dalmatian Street</td>
      <td>This series follows the lives of Delilah and D...</td>
      <td>series</td>
      <td>NaN</td>
      <td>2018–</td>
      <td>25 Mar 2019</td>
      <td>February 28, 2020</td>
      <td>NaN</td>
      <td>Animation, Comedy, Family</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Josh Brener, Michaela Dietz, Bert Davis, Abiga...</td>
      <td>English</td>
      <td>UK, USA, Canada</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.2</td>
      <td>124</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0115433</td>
      <td>101 Dalmatians</td>
      <td>An evil high-fashion designer plots to steal D...</td>
      <td>movie</td>
      <td>G</td>
      <td>1996</td>
      <td>27 Nov 1996</td>
      <td>November 12, 2019</td>
      <td>103 min</td>
      <td>Adventure, Comedy, Crime, Family</td>
      <td>Stephen Herek</td>
      <td>Dodie Smith (novel), John Hughes (screenplay)</td>
      <td>Glenn Close, Jeff Daniels, Joely Richardson, J...</td>
      <td>English, Spanish</td>
      <td>USA, UK</td>
      <td>Nominated for 1 Golden Globe. Another 3 wins &amp;...</td>
      <td>49.0</td>
      <td>5.7</td>
      <td>97,785</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0324941</td>
      <td>101 Dalmatians 2: Patch's London Adventure</td>
      <td>Being one of 101 takes its toll on Patch, who ...</td>
      <td>movie</td>
      <td>G</td>
      <td>2002</td>
      <td>21 Jan 2003</td>
      <td>November 12, 2019</td>
      <td>74 min</td>
      <td>Animation, Adventure, Comedy, Family, Musical</td>
      <td>Jim Kammerud, Brian Smith</td>
      <td>Jim Kammerud (story), Dan Root (story), Garret...</td>
      <td>Barry Bostwick, Jason Alexander, Martin Short,...</td>
      <td>English</td>
      <td>USA</td>
      <td>5 wins &amp; 10 nominations.</td>
      <td>NaN</td>
      <td>5.8</td>
      <td>7,434</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0211181</td>
      <td>102 Dalmatians</td>
      <td>Cruella DeVil gets out of prison and goes afte...</td>
      <td>movie</td>
      <td>G</td>
      <td>2000</td>
      <td>22 Nov 2000</td>
      <td>November 12, 2019</td>
      <td>100 min</td>
      <td>Adventure, Comedy, Family</td>
      <td>Kevin Lima</td>
      <td>Dodie Smith (novel), Kristen Buckley (story), ...</td>
      <td>Glenn Close, Gérard Depardieu, Ioan Gruffudd, ...</td>
      <td>English</td>
      <td>USA, UK</td>
      <td>Nominated for 1 Oscar. Another 1 win &amp; 7 nomin...</td>
      <td>35.0</td>
      <td>4.9</td>
      <td>33,444</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-51c77191-6297-4a12-9543-1f00e29c3095')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-51c77191-6297-4a12-9543-1f00e29c3095 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-51c77191-6297-4a12-9543-1f00e29c3095');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-d3bec6c7-ad5e-4e23-8996-9c813c5eec7d">
      <button class="colab-df-quickchart" onclick="quickchart('df-d3bec6c7-ad5e-4e23-8996-9c813c5eec7d')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-d3bec6c7-ad5e-4e23-8996-9c813c5eec7d button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>



##2.Basic information about dataset ##
Melihat struktur dasar data, misalnya berapa banyak kolom (Title, Type, Release Year, Rating, dll), serta tipe datanya. Supaya tahu apakah ada kolom numerik, kategorikal, atau teks


```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 992 entries, 0 to 991
    Data columns (total 19 columns):
     #   Column       Non-Null Count  Dtype  
    ---  ------       --------------  -----  
     0   imdb_id      894 non-null    object 
     1   title        894 non-null    object 
     2   plot         866 non-null    object 
     3   type         894 non-null    object 
     4   rated        742 non-null    object 
     5   year         894 non-null    object 
     6   released_at  874 non-null    object 
     7   added_at     992 non-null    object 
     8   runtime      838 non-null    object 
     9   genre        885 non-null    object 
     10  director     689 non-null    object 
     11  writer       743 non-null    object 
     12  actors       870 non-null    object 
     13  language     856 non-null    object 
     14  country      869 non-null    object 
     15  awards       556 non-null    object 
     16  metascore    292 non-null    float64
     17  imdb_rating  879 non-null    float64
     18  imdb_votes   879 non-null    object 
    dtypes: float64(2), object(17)
    memory usage: 147.4+ KB


##3.Cek Nilai Duplikat dan Unik ##
Menemukan data yang muncul lebih dari sekali (duplikat) dan menghitung variasi nilai (unik) di setiap kolom


```python
print("\nJumlah duplikat:", df.duplicated().sum())
print("\nJumlah nilai unik per kolom:")
print(df.nunique())
```

    
    Jumlah duplikat: 74
    
    Jumlah nilai unik per kolom:
    imdb_id        894
    title          872
    plot           865
    type             3
    rated           17
    year           178
    released_at    800
    added_at        58
    runtime        128
    genre          366
    director       465
    writer         710
    actors         817
    language        71
    country         59
    awards         258
    metascore       69
    imdb_rating     60
    imdb_votes     818
    dtype: int64


##4.Visualisasi jumlah unik ##
Membuat visualisasi (misal bar chart) untuk melihat distribusi jumlah nilai unik per kolom.


```python
df.nunique().plot(kind="bar", figsize=(10,4), color="#FFB6C1")
plt.title("Jumlah Nilai Unik per Kolom")
plt.show()
```


    
![png](IPSD_week_2_files/output_8_0.png)
    


##5.menemukan Null di FIles ##
Mengecek apakah ada data yang hilang (missing values).


```python
print(df.isnull().sum())
print("Dengan persentase")
print((df.isnull().mean() * 100).round(2))

```

    imdb_id         98
    title           98
    plot           126
    type            98
    rated          250
    year            98
    released_at    118
    added_at         0
    runtime        154
    genre          107
    director       303
    writer         249
    actors         122
    language       136
    country        123
    awards         436
    metascore      700
    imdb_rating    113
    imdb_votes     113
    dtype: int64
    Dengan persentase
    imdb_id         9.88
    title           9.88
    plot           12.70
    type            9.88
    rated          25.20
    year            9.88
    released_at    11.90
    added_at        0.00
    runtime        15.52
    genre          10.79
    director       30.54
    writer         25.10
    actors         12.30
    language       13.71
    country        12.40
    awards         43.95
    metascore      70.56
    imdb_rating    11.39
    imdb_votes     11.39
    dtype: float64


##6.Replace semua null values ##
Mengisi atau mengganti data yang hilang dengan nilai tertentu (mean, median, modus, atau lainnya).


```python
threshold = 0.5
for col in df.columns:
    if df[col].isnull().mean() > threshold:
        df.drop(columns=[col], inplace=True)
    else:
        if df[col].dtype == "object":
            df[col] = df[col].fillna(df[col].mode()[0])
        else:
            df[col] = df[col].fillna(df[col].median())

print("\nCek Missing Values setelah ditangani:")
print(df.isnull().sum())

```

    
    Cek Missing Values setelah ditangani:
    imdb_id        0
    title          0
    plot           0
    type           0
    rated          0
    year           0
    released_at    0
    added_at       0
    runtime        0
    genre          0
    director       0
    writer         0
    actors         0
    language       0
    country        0
    awards         0
    imdb_rating    0
    imdb_votes     0
    dtype: int64


##7.mengetahui tipe data ##
Mengetahui apakah tiap kolom berupa teks, angka, atau tanggal


```python
from google.colab import files
uploaded = files.upload()

import pandas as pd

df = pd.read_csv("disney_plus_shows.csv")

print("Tipe data setiap kolom:\n")
df_types = pd.DataFrame({
    "Kolom": df.columns,
    "Tipe Data": df.dtypes.astype(str)
})

display(df_types)
```



     <input type="file" id="files-e8aaa56b-6a8b-4f29-8805-095c7626005c" name="files[]" multiple disabled
        style="border:none" />
     <output id="result-e8aaa56b-6a8b-4f29-8805-095c7626005c">
      Upload widget is only available when the cell has been executed in the
      current browser session. Please rerun this cell to enable.
      </output>
      <script>// Copyright 2017 Google LLC
//
// Licensed under the Apache License, Version 2.0 (the "License");
// you may not use this file except in compliance with the License.
// You may obtain a copy of the License at
//
//      http://www.apache.org/licenses/LICENSE-2.0
//
// Unless required by applicable law or agreed to in writing, software
// distributed under the License is distributed on an "AS IS" BASIS,
// WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
// See the License for the specific language governing permissions and
// limitations under the License.

/**
 * @fileoverview Helpers for google.colab Python module.
 */
(function(scope) {
function span(text, styleAttributes = {}) {
  const element = document.createElement('span');
  element.textContent = text;
  for (const key of Object.keys(styleAttributes)) {
    element.style[key] = styleAttributes[key];
  }
  return element;
}

// Max number of bytes which will be uploaded at a time.
const MAX_PAYLOAD_SIZE = 100 * 1024;

function _uploadFiles(inputId, outputId) {
  const steps = uploadFilesStep(inputId, outputId);
  const outputElement = document.getElementById(outputId);
  // Cache steps on the outputElement to make it available for the next call
  // to uploadFilesContinue from Python.
  outputElement.steps = steps;

  return _uploadFilesContinue(outputId);
}

// This is roughly an async generator (not supported in the browser yet),
// where there are multiple asynchronous steps and the Python side is going
// to poll for completion of each step.
// This uses a Promise to block the python side on completion of each step,
// then passes the result of the previous step as the input to the next step.
function _uploadFilesContinue(outputId) {
  const outputElement = document.getElementById(outputId);
  const steps = outputElement.steps;

  const next = steps.next(outputElement.lastPromiseValue);
  return Promise.resolve(next.value.promise).then((value) => {
    // Cache the last promise value to make it available to the next
    // step of the generator.
    outputElement.lastPromiseValue = value;
    return next.value.response;
  });
}

/**
 * Generator function which is called between each async step of the upload
 * process.
 * @param {string} inputId Element ID of the input file picker element.
 * @param {string} outputId Element ID of the output display.
 * @return {!Iterable<!Object>} Iterable of next steps.
 */
function* uploadFilesStep(inputId, outputId) {
  const inputElement = document.getElementById(inputId);
  inputElement.disabled = false;

  const outputElement = document.getElementById(outputId);
  outputElement.innerHTML = '';

  const pickedPromise = new Promise((resolve) => {
    inputElement.addEventListener('change', (e) => {
      resolve(e.target.files);
    });
  });

  const cancel = document.createElement('button');
  inputElement.parentElement.appendChild(cancel);
  cancel.textContent = 'Cancel upload';
  const cancelPromise = new Promise((resolve) => {
    cancel.onclick = () => {
      resolve(null);
    };
  });

  // Wait for the user to pick the files.
  const files = yield {
    promise: Promise.race([pickedPromise, cancelPromise]),
    response: {
      action: 'starting',
    }
  };

  cancel.remove();

  // Disable the input element since further picks are not allowed.
  inputElement.disabled = true;

  if (!files) {
    return {
      response: {
        action: 'complete',
      }
    };
  }

  for (const file of files) {
    const li = document.createElement('li');
    li.append(span(file.name, {fontWeight: 'bold'}));
    li.append(span(
        `(${file.type || 'n/a'}) - ${file.size} bytes, ` +
        `last modified: ${
            file.lastModifiedDate ? file.lastModifiedDate.toLocaleDateString() :
                                    'n/a'} - `));
    const percent = span('0% done');
    li.appendChild(percent);

    outputElement.appendChild(li);

    const fileDataPromise = new Promise((resolve) => {
      const reader = new FileReader();
      reader.onload = (e) => {
        resolve(e.target.result);
      };
      reader.readAsArrayBuffer(file);
    });
    // Wait for the data to be ready.
    let fileData = yield {
      promise: fileDataPromise,
      response: {
        action: 'continue',
      }
    };

    // Use a chunked sending to avoid message size limits. See b/62115660.
    let position = 0;
    do {
      const length = Math.min(fileData.byteLength - position, MAX_PAYLOAD_SIZE);
      const chunk = new Uint8Array(fileData, position, length);
      position += length;

      const base64 = btoa(String.fromCharCode.apply(null, chunk));
      yield {
        response: {
          action: 'append',
          file: file.name,
          data: base64,
        },
      };

      let percentDone = fileData.byteLength === 0 ?
          100 :
          Math.round((position / fileData.byteLength) * 100);
      percent.textContent = `${percentDone}% done`;

    } while (position < fileData.byteLength);
  }

  // All done.
  yield {
    response: {
      action: 'complete',
    }
  };
}

scope.google = scope.google || {};
scope.google.colab = scope.google.colab || {};
scope.google.colab._files = {
  _uploadFiles,
  _uploadFilesContinue,
};
})(self);
</script> 


    Saving disney_plus_shows.csv to disney_plus_shows (2).csv
    Tipe data setiap kolom:
    




  <div id="df-dda1b672-ee0f-4fbb-8bd6-18a52f42dc58" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Kolom</th>
      <th>Tipe Data</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>imdb_id</th>
      <td>imdb_id</td>
      <td>object</td>
    </tr>
    <tr>
      <th>title</th>
      <td>title</td>
      <td>object</td>
    </tr>
    <tr>
      <th>plot</th>
      <td>plot</td>
      <td>object</td>
    </tr>
    <tr>
      <th>type</th>
      <td>type</td>
      <td>object</td>
    </tr>
    <tr>
      <th>rated</th>
      <td>rated</td>
      <td>object</td>
    </tr>
    <tr>
      <th>year</th>
      <td>year</td>
      <td>object</td>
    </tr>
    <tr>
      <th>released_at</th>
      <td>released_at</td>
      <td>object</td>
    </tr>
    <tr>
      <th>added_at</th>
      <td>added_at</td>
      <td>object</td>
    </tr>
    <tr>
      <th>runtime</th>
      <td>runtime</td>
      <td>object</td>
    </tr>
    <tr>
      <th>genre</th>
      <td>genre</td>
      <td>object</td>
    </tr>
    <tr>
      <th>director</th>
      <td>director</td>
      <td>object</td>
    </tr>
    <tr>
      <th>writer</th>
      <td>writer</td>
      <td>object</td>
    </tr>
    <tr>
      <th>actors</th>
      <td>actors</td>
      <td>object</td>
    </tr>
    <tr>
      <th>language</th>
      <td>language</td>
      <td>object</td>
    </tr>
    <tr>
      <th>country</th>
      <td>country</td>
      <td>object</td>
    </tr>
    <tr>
      <th>awards</th>
      <td>awards</td>
      <td>object</td>
    </tr>
    <tr>
      <th>metascore</th>
      <td>metascore</td>
      <td>float64</td>
    </tr>
    <tr>
      <th>imdb_rating</th>
      <td>imdb_rating</td>
      <td>float64</td>
    </tr>
    <tr>
      <th>imdb_votes</th>
      <td>imdb_votes</td>
      <td>object</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-dda1b672-ee0f-4fbb-8bd6-18a52f42dc58')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-dda1b672-ee0f-4fbb-8bd6-18a52f42dc58 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-dda1b672-ee0f-4fbb-8bd6-18a52f42dc58');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-de787be3-b61a-41f0-ad12-12f613d31dc1">
      <button class="colab-df-quickchart" onclick="quickchart('df-de787be3-b61a-41f0-ad12-12f613d31dc1')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-de787be3-b61a-41f0-ad12-12f613d31dc1 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

  <div id="id_42958636-6ad7-407b-b012-ccfa6a13af5b">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('df_types')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_42958636-6ad7-407b-b012-ccfa6a13af5b button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('df_types');
      }
      })();
    </script>
  </div>

    </div>
  </div>



##8.FIlter Data ##

mensortir data untuk menentukan mana tabel yang bisa di visualisasi dan korelasi



```python
df_types = pd.DataFrame({
    "Kolom": df.columns,
    "Tipe Data": df.dtypes.astype(str),
    "Jumlah Unik": df.nunique(),
    "Jumlah Missing": df.isnull().sum()
})

df_types.head(len(df_types))
```





  <div id="df-140b16e8-4e90-41cd-aae7-aae282c1e7a4" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Kolom</th>
      <th>Tipe Data</th>
      <th>Jumlah Unik</th>
      <th>Jumlah Missing</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>imdb_id</th>
      <td>imdb_id</td>
      <td>object</td>
      <td>894</td>
      <td>98</td>
    </tr>
    <tr>
      <th>title</th>
      <td>title</td>
      <td>object</td>
      <td>872</td>
      <td>98</td>
    </tr>
    <tr>
      <th>plot</th>
      <td>plot</td>
      <td>object</td>
      <td>865</td>
      <td>126</td>
    </tr>
    <tr>
      <th>type</th>
      <td>type</td>
      <td>object</td>
      <td>3</td>
      <td>98</td>
    </tr>
    <tr>
      <th>rated</th>
      <td>rated</td>
      <td>object</td>
      <td>17</td>
      <td>250</td>
    </tr>
    <tr>
      <th>year</th>
      <td>year</td>
      <td>object</td>
      <td>178</td>
      <td>98</td>
    </tr>
    <tr>
      <th>released_at</th>
      <td>released_at</td>
      <td>object</td>
      <td>800</td>
      <td>118</td>
    </tr>
    <tr>
      <th>added_at</th>
      <td>added_at</td>
      <td>object</td>
      <td>58</td>
      <td>0</td>
    </tr>
    <tr>
      <th>runtime</th>
      <td>runtime</td>
      <td>object</td>
      <td>128</td>
      <td>154</td>
    </tr>
    <tr>
      <th>genre</th>
      <td>genre</td>
      <td>object</td>
      <td>366</td>
      <td>107</td>
    </tr>
    <tr>
      <th>director</th>
      <td>director</td>
      <td>object</td>
      <td>465</td>
      <td>303</td>
    </tr>
    <tr>
      <th>writer</th>
      <td>writer</td>
      <td>object</td>
      <td>710</td>
      <td>249</td>
    </tr>
    <tr>
      <th>actors</th>
      <td>actors</td>
      <td>object</td>
      <td>817</td>
      <td>122</td>
    </tr>
    <tr>
      <th>language</th>
      <td>language</td>
      <td>object</td>
      <td>71</td>
      <td>136</td>
    </tr>
    <tr>
      <th>country</th>
      <td>country</td>
      <td>object</td>
      <td>59</td>
      <td>123</td>
    </tr>
    <tr>
      <th>awards</th>
      <td>awards</td>
      <td>object</td>
      <td>258</td>
      <td>436</td>
    </tr>
    <tr>
      <th>metascore</th>
      <td>metascore</td>
      <td>float64</td>
      <td>69</td>
      <td>700</td>
    </tr>
    <tr>
      <th>imdb_rating</th>
      <td>imdb_rating</td>
      <td>float64</td>
      <td>60</td>
      <td>113</td>
    </tr>
    <tr>
      <th>imdb_votes</th>
      <td>imdb_votes</td>
      <td>object</td>
      <td>818</td>
      <td>113</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-140b16e8-4e90-41cd-aae7-aae282c1e7a4')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-140b16e8-4e90-41cd-aae7-aae282c1e7a4 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-140b16e8-4e90-41cd-aae7-aae282c1e7a4');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-88eb3a43-1f39-4a90-8ded-2a94d32c8c87">
      <button class="colab-df-quickchart" onclick="quickchart('df-88eb3a43-1f39-4a90-8ded-2a94d32c8c87')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-88eb3a43-1f39-4a90-8ded-2a94d32c8c87 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>




##9.Create Box Plot ##
Membuat visualisasi box plot untuk melihat persebaran data, outlier, serta nilai median dan kuartil. Berguna untuk memahami distribusi data numerik.


```python
df.head(5)
```





  <div id="df-085ba88f-4326-4cfc-bc74-f406e4a68e19" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>imdb_id</th>
      <th>title</th>
      <th>plot</th>
      <th>type</th>
      <th>rated</th>
      <th>year</th>
      <th>released_at</th>
      <th>added_at</th>
      <th>runtime</th>
      <th>genre</th>
      <th>director</th>
      <th>writer</th>
      <th>actors</th>
      <th>language</th>
      <th>country</th>
      <th>awards</th>
      <th>metascore</th>
      <th>imdb_rating</th>
      <th>imdb_votes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0147800</td>
      <td>10 Things I Hate About You</td>
      <td>A pretty, popular teenager can't go out on a d...</td>
      <td>movie</td>
      <td>PG-13</td>
      <td>1999</td>
      <td>31 Mar 1999</td>
      <td>November 12, 2019</td>
      <td>97 min</td>
      <td>Comedy, Drama, Romance</td>
      <td>Gil Junger</td>
      <td>Karen McCullah, Kirsten Smith</td>
      <td>Heath Ledger, Julia Stiles, Joseph Gordon-Levi...</td>
      <td>English, French</td>
      <td>USA</td>
      <td>2 wins &amp; 13 nominations.</td>
      <td>70.0</td>
      <td>7.3</td>
      <td>283,945</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt7019028</td>
      <td>101 Dalmatian Street</td>
      <td>This series follows the lives of Delilah and D...</td>
      <td>series</td>
      <td>NaN</td>
      <td>2018–</td>
      <td>25 Mar 2019</td>
      <td>February 28, 2020</td>
      <td>NaN</td>
      <td>Animation, Comedy, Family</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Josh Brener, Michaela Dietz, Bert Davis, Abiga...</td>
      <td>English</td>
      <td>UK, USA, Canada</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>6.2</td>
      <td>124</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0115433</td>
      <td>101 Dalmatians</td>
      <td>An evil high-fashion designer plots to steal D...</td>
      <td>movie</td>
      <td>G</td>
      <td>1996</td>
      <td>27 Nov 1996</td>
      <td>November 12, 2019</td>
      <td>103 min</td>
      <td>Adventure, Comedy, Crime, Family</td>
      <td>Stephen Herek</td>
      <td>Dodie Smith (novel), John Hughes (screenplay)</td>
      <td>Glenn Close, Jeff Daniels, Joely Richardson, J...</td>
      <td>English, Spanish</td>
      <td>USA, UK</td>
      <td>Nominated for 1 Golden Globe. Another 3 wins &amp;...</td>
      <td>49.0</td>
      <td>5.7</td>
      <td>97,785</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0324941</td>
      <td>101 Dalmatians 2: Patch's London Adventure</td>
      <td>Being one of 101 takes its toll on Patch, who ...</td>
      <td>movie</td>
      <td>G</td>
      <td>2002</td>
      <td>21 Jan 2003</td>
      <td>November 12, 2019</td>
      <td>74 min</td>
      <td>Animation, Adventure, Comedy, Family, Musical</td>
      <td>Jim Kammerud, Brian Smith</td>
      <td>Jim Kammerud (story), Dan Root (story), Garret...</td>
      <td>Barry Bostwick, Jason Alexander, Martin Short,...</td>
      <td>English</td>
      <td>USA</td>
      <td>5 wins &amp; 10 nominations.</td>
      <td>NaN</td>
      <td>5.8</td>
      <td>7,434</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0211181</td>
      <td>102 Dalmatians</td>
      <td>Cruella DeVil gets out of prison and goes afte...</td>
      <td>movie</td>
      <td>G</td>
      <td>2000</td>
      <td>22 Nov 2000</td>
      <td>November 12, 2019</td>
      <td>100 min</td>
      <td>Adventure, Comedy, Family</td>
      <td>Kevin Lima</td>
      <td>Dodie Smith (novel), Kristen Buckley (story), ...</td>
      <td>Glenn Close, Gérard Depardieu, Ioan Gruffudd, ...</td>
      <td>English</td>
      <td>USA, UK</td>
      <td>Nominated for 1 Oscar. Another 1 win &amp; 7 nomin...</td>
      <td>35.0</td>
      <td>4.9</td>
      <td>33,444</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-085ba88f-4326-4cfc-bc74-f406e4a68e19')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-085ba88f-4326-4cfc-bc74-f406e4a68e19 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-085ba88f-4326-4cfc-bc74-f406e4a68e19');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-3b55e203-94f8-460d-808c-7bc6ad72d7cc">
      <button class="colab-df-quickchart" onclick="quickchart('df-3b55e203-94f8-460d-808c-7bc6ad72d7cc')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-3b55e203-94f8-460d-808c-7bc6ad72d7cc button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>





```python
import seaborn as sns
import matplotlib.pyplot as plt

plt.figure(figsize=(10, 6))
sns.boxplot(x='type', y='imdb_rating', data=df)
plt.title('Boxplot IMDb Rating by Content Type')
plt.xlabel('Content Type')
plt.ylabel('IMDb Rating')
plt.show()
```


    
![png](IPSD_week_2_files/output_19_0.png)
    



```python
from google.colab import files
uploaded = files.upload()
```



     <input type="file" id="files-2d64aba9-f474-4251-816e-7da6dc12e0fc" name="files[]" multiple disabled
        style="border:none" />
     <output id="result-2d64aba9-f474-4251-816e-7da6dc12e0fc">
      Upload widget is only available when the cell has been executed in the
      current browser session. Please rerun this cell to enable.
      </output>
      <script>// Copyright 2017 Google LLC
//
// Licensed under the Apache License, Version 2.0 (the "License");
// you may not use this file except in compliance with the License.
// You may obtain a copy of the License at
//
//      http://www.apache.org/licenses/LICENSE-2.0
//
// Unless required by applicable law or agreed to in writing, software
// distributed under the License is distributed on an "AS IS" BASIS,
// WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
// See the License for the specific language governing permissions and
// limitations under the License.

/**
 * @fileoverview Helpers for google.colab Python module.
 */
(function(scope) {
function span(text, styleAttributes = {}) {
  const element = document.createElement('span');
  element.textContent = text;
  for (const key of Object.keys(styleAttributes)) {
    element.style[key] = styleAttributes[key];
  }
  return element;
}

// Max number of bytes which will be uploaded at a time.
const MAX_PAYLOAD_SIZE = 100 * 1024;

function _uploadFiles(inputId, outputId) {
  const steps = uploadFilesStep(inputId, outputId);
  const outputElement = document.getElementById(outputId);
  // Cache steps on the outputElement to make it available for the next call
  // to uploadFilesContinue from Python.
  outputElement.steps = steps;

  return _uploadFilesContinue(outputId);
}

// This is roughly an async generator (not supported in the browser yet),
// where there are multiple asynchronous steps and the Python side is going
// to poll for completion of each step.
// This uses a Promise to block the python side on completion of each step,
// then passes the result of the previous step as the input to the next step.
function _uploadFilesContinue(outputId) {
  const outputElement = document.getElementById(outputId);
  const steps = outputElement.steps;

  const next = steps.next(outputElement.lastPromiseValue);
  return Promise.resolve(next.value.promise).then((value) => {
    // Cache the last promise value to make it available to the next
    // step of the generator.
    outputElement.lastPromiseValue = value;
    return next.value.response;
  });
}

/**
 * Generator function which is called between each async step of the upload
 * process.
 * @param {string} inputId Element ID of the input file picker element.
 * @param {string} outputId Element ID of the output display.
 * @return {!Iterable<!Object>} Iterable of next steps.
 */
function* uploadFilesStep(inputId, outputId) {
  const inputElement = document.getElementById(inputId);
  inputElement.disabled = false;

  const outputElement = document.getElementById(outputId);
  outputElement.innerHTML = '';

  const pickedPromise = new Promise((resolve) => {
    inputElement.addEventListener('change', (e) => {
      resolve(e.target.files);
    });
  });

  const cancel = document.createElement('button');
  inputElement.parentElement.appendChild(cancel);
  cancel.textContent = 'Cancel upload';
  const cancelPromise = new Promise((resolve) => {
    cancel.onclick = () => {
      resolve(null);
    };
  });

  // Wait for the user to pick the files.
  const files = yield {
    promise: Promise.race([pickedPromise, cancelPromise]),
    response: {
      action: 'starting',
    }
  };

  cancel.remove();

  // Disable the input element since further picks are not allowed.
  inputElement.disabled = true;

  if (!files) {
    return {
      response: {
        action: 'complete',
      }
    };
  }

  for (const file of files) {
    const li = document.createElement('li');
    li.append(span(file.name, {fontWeight: 'bold'}));
    li.append(span(
        `(${file.type || 'n/a'}) - ${file.size} bytes, ` +
        `last modified: ${
            file.lastModifiedDate ? file.lastModifiedDate.toLocaleDateString() :
                                    'n/a'} - `));
    const percent = span('0% done');
    li.appendChild(percent);

    outputElement.appendChild(li);

    const fileDataPromise = new Promise((resolve) => {
      const reader = new FileReader();
      reader.onload = (e) => {
        resolve(e.target.result);
      };
      reader.readAsArrayBuffer(file);
    });
    // Wait for the data to be ready.
    let fileData = yield {
      promise: fileDataPromise,
      response: {
        action: 'continue',
      }
    };

    // Use a chunked sending to avoid message size limits. See b/62115660.
    let position = 0;
    do {
      const length = Math.min(fileData.byteLength - position, MAX_PAYLOAD_SIZE);
      const chunk = new Uint8Array(fileData, position, length);
      position += length;

      const base64 = btoa(String.fromCharCode.apply(null, chunk));
      yield {
        response: {
          action: 'append',
          file: file.name,
          data: base64,
        },
      };

      let percentDone = fileData.byteLength === 0 ?
          100 :
          Math.round((position / fileData.byteLength) * 100);
      percent.textContent = `${percentDone}% done`;

    } while (position < fileData.byteLength);
  }

  // All done.
  yield {
    response: {
      action: 'complete',
    }
  };
}

scope.google = scope.google || {};
scope.google.colab = scope.google.colab || {};
scope.google.colab._files = {
  _uploadFiles,
  _uploadFilesContinue,
};
})(self);
</script> 


    Saving disney_plus_shows.csv to disney_plus_shows (3).csv



```python

display(df.head())
```



  <div id="df-e061b628-ed41-4545-beca-6e01a59c2ccf" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>imdb_id</th>
      <th>title</th>
      <th>plot</th>
      <th>type</th>
      <th>rated</th>
      <th>year</th>
      <th>released_at</th>
      <th>added_at</th>
      <th>runtime</th>
      <th>genre</th>
      <th>director</th>
      <th>writer</th>
      <th>actors</th>
      <th>language</th>
      <th>country</th>
      <th>awards</th>
      <th>imdb_rating</th>
      <th>imdb_votes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0147800</td>
      <td>10 Things I Hate About You</td>
      <td>A pretty, popular teenager can't go out on a d...</td>
      <td>movie</td>
      <td>PG-13</td>
      <td>1999</td>
      <td>31 Mar 1999</td>
      <td>November 12, 2019</td>
      <td>97 min</td>
      <td>Comedy, Drama, Romance</td>
      <td>Gil Junger</td>
      <td>Karen McCullah, Kirsten Smith</td>
      <td>Heath Ledger, Julia Stiles, Joseph Gordon-Levi...</td>
      <td>English, French</td>
      <td>USA</td>
      <td>2 wins &amp; 13 nominations.</td>
      <td>7.3</td>
      <td>283,945</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt7019028</td>
      <td>101 Dalmatian Street</td>
      <td>This series follows the lives of Delilah and D...</td>
      <td>series</td>
      <td>G</td>
      <td>2018–</td>
      <td>25 Mar 2019</td>
      <td>February 28, 2020</td>
      <td>30 min</td>
      <td>Animation, Comedy, Family</td>
      <td>Jack Hannah</td>
      <td>Bill Berg (story), Nick George (story)</td>
      <td>Josh Brener, Michaela Dietz, Bert Davis, Abiga...</td>
      <td>English</td>
      <td>UK, USA, Canada</td>
      <td>1 nomination.</td>
      <td>6.2</td>
      <td>124</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0115433</td>
      <td>101 Dalmatians</td>
      <td>An evil high-fashion designer plots to steal D...</td>
      <td>movie</td>
      <td>G</td>
      <td>1996</td>
      <td>27 Nov 1996</td>
      <td>November 12, 2019</td>
      <td>103 min</td>
      <td>Adventure, Comedy, Crime, Family</td>
      <td>Stephen Herek</td>
      <td>Dodie Smith (novel), John Hughes (screenplay)</td>
      <td>Glenn Close, Jeff Daniels, Joely Richardson, J...</td>
      <td>English, Spanish</td>
      <td>USA, UK</td>
      <td>Nominated for 1 Golden Globe. Another 3 wins &amp;...</td>
      <td>5.7</td>
      <td>97,785</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0324941</td>
      <td>101 Dalmatians 2: Patch's London Adventure</td>
      <td>Being one of 101 takes its toll on Patch, who ...</td>
      <td>movie</td>
      <td>G</td>
      <td>2002</td>
      <td>21 Jan 2003</td>
      <td>November 12, 2019</td>
      <td>74 min</td>
      <td>Animation, Adventure, Comedy, Family, Musical</td>
      <td>Jim Kammerud, Brian Smith</td>
      <td>Jim Kammerud (story), Dan Root (story), Garret...</td>
      <td>Barry Bostwick, Jason Alexander, Martin Short,...</td>
      <td>English</td>
      <td>USA</td>
      <td>5 wins &amp; 10 nominations.</td>
      <td>5.8</td>
      <td>7,434</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0211181</td>
      <td>102 Dalmatians</td>
      <td>Cruella DeVil gets out of prison and goes afte...</td>
      <td>movie</td>
      <td>G</td>
      <td>2000</td>
      <td>22 Nov 2000</td>
      <td>November 12, 2019</td>
      <td>100 min</td>
      <td>Adventure, Comedy, Family</td>
      <td>Kevin Lima</td>
      <td>Dodie Smith (novel), Kristen Buckley (story), ...</td>
      <td>Glenn Close, Gérard Depardieu, Ioan Gruffudd, ...</td>
      <td>English</td>
      <td>USA, UK</td>
      <td>Nominated for 1 Oscar. Another 1 win &amp; 7 nomin...</td>
      <td>4.9</td>
      <td>33,444</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-e061b628-ed41-4545-beca-6e01a59c2ccf')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-e061b628-ed41-4545-beca-6e01a59c2ccf button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-e061b628-ed41-4545-beca-6e01a59c2ccf');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-6f5aa6bc-b387-46ff-9d4c-72facddf2f25">
      <button class="colab-df-quickchart" onclick="quickchart('df-6f5aa6bc-b387-46ff-9d4c-72facddf2f25')"
                title="Suggest charts"
                style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-6f5aa6bc-b387-46ff-9d4c-72facddf2f25 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>




```python
threshold = 0.5
for col in df.columns:
    if df[col].isnull().mean() > threshold:
        df.drop(columns=[col], inplace=True)
    else:
        if df[col].dtype == "object":
            df[col] = df[col].fillna(df[col].mode()[0])
        else:
            df[col] = df[col].fillna(df[col].median())

print("\nCek Missing Values setelah ditangani:")
print(df.isnull().sum())
```

    
    Cek Missing Values setelah ditangani:
    imdb_id        0
    title          0
    plot           0
    type           0
    rated          0
    year           0
    released_at    0
    added_at       0
    runtime        0
    genre          0
    director       0
    writer         0
    actors         0
    language       0
    country        0
    awards         0
    imdb_rating    0
    imdb_votes     0
    dtype: int64


##10.Correlation ##
Menghitung dan memvisualisasikan hubungan antar variabel numerik pada dataset


```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv('/content/disney_plus_shows.csv')
correlation_matrix = df.corr(numeric_only=True)

plt.figure(figsize=(10, 8))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt=".2f")
plt.title('Correlation Matrix')
plt.show()
```


    
![png](IPSD_week_2_files/output_24_0.png)
    



```python

```
