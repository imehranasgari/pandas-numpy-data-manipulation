# Machine Learning in Python: Pandas Data Selection and NumPy Basics

This project contains Jupyter notebooks demonstrating fundamental data manipulation and numerical computing techniques using Pandas and NumPy libraries in Python.

## Technologies & Libraries

*   **Python**
*   **Pandas**: Used for data manipulation and analysis, particularly with DataFrames.
*   **NumPy**: Utilized for numerical operations and array manipulation.
*   **Jupyter Notebook**: The environment where the code is written and executed.

## Installation & Execution Guide

### Prerequisites

*   Python installed on your system.
*   Jupyter Notebook installed.

### Library Installation

You can install the necessary libraries using `pip` or `conda`:

*   **NumPy**:
    ```bash
    !conda install numpy
    ```
    or
    ```bash
    !pip install numpy
    ```
*   **Pandas**:
    ```bash
    !pip install pandas
    ```

### Data

The project uses a `titanic.csv` dataset. Ensure this file is in the same directory as your Jupyter notebooks, or update the file path in the notebooks accordingly.

### Running the Notebooks

1.  **Clone the repository** (if applicable, otherwise ensure you have the notebook files).
2.  **Navigate to the project directory** in your terminal.
3.  **Start Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```
4.  **Open the desired notebook** (`loc_iloc.ipynb` or `Pandas.ipynb` or `Numpy.ipynb`) from the Jupyter interface in your web browser.
5.  **Run the cells** sequentially to execute the code and see the demonstrations.

## Screenshots / Sample Outputs

### Pandas Data Selection (`loc_iloc.ipynb`)

*   **Sample of the Titanic DataFrame:**
    ```
          pclass  survived                          name     sex   age  sibsp  parch   ticket     fare cabin embarked boat   body home.dest
    1183       3         0     Salonen, Mr. Johan Werner    male  39.0      0      0  3101296   7.9250   NaN        S  NaN    NaN       NaN
    1101       3         0  Panula, Master. Eino Viljami    male   1.0      4      1  3101295  39.6875   NaN        S  NaN    NaN       NaN
    833        3         0       Green, Mr. George Henry    male  51.0      0      0    21440   8.0500   NaN        S  NaN    NaN  Dorking, Surrey, England
    584        2         1           Webber, Miss. Susan  female  32.5      0      0    27267  13.0000  E101        S   12    NaN    England / Hartford, CT
    716        3         0   Chronopoulos, Mr. Apostolos    male  26.0      1      0     2680  14.4542   NaN        C  NaN    NaN                    Greece
    ```
*   **Selecting a single column (`age`):**
    ```
    0       29.00
    1        0.92
    2        2.00
    3       30.00
    4       25.00
            ...
    1304    14.50
    1305      NaN
    1306    26.50
    1307    27.00
    1308    29.00
    Name: age, Length: 1309, dtype: float64
    ```
*   **Selecting multiple columns (`age`, `pclass`, `fare`):**
    ```
            age  pclass      fare
    0     29.00       1  211.3375
    1      0.92       1  151.5500
    2      2.00       1  151.5500
    3     30.00       1  151.5500
    4     25.00       1  151.5500
    ...     ...     ...       ...
    1304  14.50       3   14.4542
    1305    NaN       3   14.4542
    1306  26.50       3    7.2250
    1307  27.00       3    7.2250
    1308  29.00       3    7.8750
    [1309 rows x 3 columns]
    ```
*   **Selecting specific rows and columns using `iloc`:**
    ```
       survived                                             name  parch
    3         0             Allison, Mr. Hudson Joshua Creighton      2
    4         0  Allison, Mrs. Hudson J C (Bessie Waldo Daniels)      2
    ```
*   **Selecting rows and columns using slicing with `iloc`:**
    ```
                                                     name     sex   age
    9                             Artagaveytia, Mr. Ramon    male  71.0
    10                             Astor, Col. John Jacob    male  47.0
    11  Astor, Mrs. John Jacob (Madeleine Talmadge Force)  female  18.0
    12                      Aubart, Mme. Leontine Pauline  female  24.0
    13                       Barber, Miss. Ellen "Nellie"  female  26.0
    14               Barkworth, Mr. Algernon Henry Wilson    male  80.0
    15                                Baumann, Mr. John D    male   NaN
    16                           Baxter, Mr. Quigg Edmond    male  24.0
    17    Baxter, Mrs. James (Helene DeLaudeniere Chaput)  female  50.0
    18                              Bazzani, Miss. Albina  female  32.0
    19                               Beattie, Mr. Thomson    male  36.0
    20                      Beckwith, Mr. Richard Leonard    male  37.0
    21   Beckwith, Mrs. Richard Leonard (Sallie Monypeny)  female  47.0
    22                              Behr, Mr. Karl Howell    male  26.0
    23                              Bidois, Miss. Rosalie  female  42.0
    24                                  Bird, Miss. Ellen  female  29.0
    ```
*   **Conditional selection using `loc` and boolean indexing:**
    ```
         pclass  survived                                               name     sex   age  sibsp  parch    ticket      fare        cabin embarked  boat  body     home.dest
    0         1         1                      Allen, Miss. Elisabeth Walton  female  29.0      0      0     24160  211.3375           B5        S     2   NaN  St Louis, MO
    24        1         1                                  Bird, Miss. Ellen  female  29.0      0      0  PC 17483  221.7792          C97        S     8   NaN           NaN
    111       1         1                     Fortune, Miss. Alice Elizabeth  female  24.0      3      2     19950  263.0000  C23 C25 C27        S    10   NaN  Winnipeg, MB
    112       1         1                         Fortune, Miss. Ethel Flora  female  28.0      3      2     19950  263.0000  C23 C25 C27        S    10   NaN  Winnipeg, MB
    113       1         1                         Fortune, Miss. Mabel Helen  female  23.0      3      2     19950  263.0000  C23 C25 C27        S    10   NaN  Winnipeg, MB
    116       1         1                Fortune, Mrs. Mark (Mary McDougald)  female  60.0      1      4     19950  263.0000  C23 C25 C27        S    10   NaN  Winnipeg, MB
    180       1         1                             Kreuchen, Miss. Emilie  female  39.0      0      0     24160  211.3375          NaN        S     2   NaN           NaN
    193       1         1                  Madill, Miss. Georgette Alexandra  female  15.0      0      1     24160  211.3375           B5        S     2   NaN  St Louis, MO
    238       1         1  Robert, Mrs. Edward Scott (Elisabeth Walton Mc...  female  43.0      0      1     24160  211.3375           B3        S     2   NaN  St Louis, MO
    ```

### Pandas Basics (`Pandas.ipynb`)

*   **Displaying the first 5 rows (`.head()`):**
    ```
       pclass  survived                                             name     sex    age  sibsp  parch  ticket      fare    cabin embarked boat   body                        home.dest
    0       1         1                    Allen, Miss. Elisabeth Walton  female  29.00      0      0   24160  211.3375       B5        S    2    NaN                     St Louis, MO
    1       1         1                   Allison, Master. Hudson Trevor    male   0.92      1      2  113781  151.5500  C22 C26        S   11    NaN  Montreal, PQ / Chesterville, ON
    2       1         0                     Allison, Miss. Helen Loraine  female   2.00      1      2  113781  151.5500  C22 C26        S  NaN    NaN  Montreal, PQ / Chesterville, ON
    3       1         0             Allison, Mr. Hudson Joshua Creighton    male  30.00      1      2  113781  151.5500  C22 C26        S  NaN  135.0  Montreal, PQ / Chesterville, ON
    4       1         0  Allison, Mrs. Hudson J C (Bessie Waldo Daniels)  female  25.00      1      2  113781  151.5500  C22 C26        S  NaN    NaN  Montreal, PQ / Chesterville, ON
    ```
*   **DataFrame shape:**
    ```
    (1309, 14)
    ```
*   **Column names:**
    ```
    Index(['pclass', 'survived', 'name', 'sex', 'age', 'sibsp', 'parch', 'ticket',
           'fare', 'cabin', 'embarked', 'boat', 'body', 'home.dest'],
          dtype='object')
    ```
*   **Data types of columns:**
    ```
    pclass         int64
    survived       int64
    name          object
    sex           object
    age          float64
    sibsp          int64
    parch          int64
    ticket        object
    fare         float64
    cabin         object
    embarked      object
    boat          object
    body         float64
    home.dest     object
    dtype: object
    ```
*   **Value counts for 'survived' column:**
    ```
    0    809
    1    500
    Name: survived, dtype: int64
    ```
*   **Normalized value counts for 'survived' column (percentage):**
    ```
    0    61.802903
    1    38.197097
    Name: survived, dtype: float64
    ```
*   **Crosstabulation of 'sex' and 'survived':**
    ```
    survived    0    1
    sex
    female    127  339
    male      682  161
    ```
*   **Passengers with 'Allen' in their name:**
    ```
         pclass  survived                                              name     sex   age  sibsp  parch  ticket      fare cabin embarked boat  body                                  home.dest
    0         1         1                     Allen, Miss. Elisabeth Walton  female  29.0      0      0   24160  211.3375    B5        S    2   NaN                               St Louis, MO
    342       2         1  Becker, Mrs. Allen Oliver (Nellie E Baumgardner)  female  36.0      0      3  230136   39.0000    F4        S   11   NaN                 Guntur, India / Benton Harbour, MI
    618       3         0                          Allen, Mr. William Henry    male  35.0      0      0  373450    8.0500   NaN        S  NaN   NaN  Lower Clapton, Middlesex or Erdington, Birmingham
    ```
*   **Unique values in 'embarked' column:**
    ```
    array(['S', 'C', nan, 'Q'], dtype=object)
    ```
*   **Mean fare grouped by 'pclass':**
    ```
    pclass
    1    87.508992
    2    21.179196
    3    13.302889
    Name: fare, dtype: float64
    ```
*   **Mean age grouped by 'pclass':**
    ```
       pclass        age
    0       1  39.159930
    1       2  29.506705
    2       3  24.816367
    ```
*   **Sorted DataFrame by 'age' (descending):**
    ```
          pclass  survived                                               name     sex   age  sibsp  parch    ticket      fare cabin embarked boat  body                home.dest
    14         1         1               Barkworth, Mr. Algernon Henry Wilson    male  80.0      0      0       27042  30.0000   A23        S    B   NaN            Hessle, Yorks
    61         1         1  Cavendish, Mrs. Tyrell William (Julia Florence...  female  76.0      1      0       19877  78.8500   C46        S    6   NaN  Little Onn Hall, Staffs
    1235       3         0                                Svensson, Mr. Johan    male  74.0      0      0      347060   7.7750   NaN        S  NaN   NaN                      NaN
    135        1         0                          Goldschmidt, Mr. George B    male  71.0      0      0    PC 17754  34.6542    A5        C  NaN   NaN             New York, NY
    9          1         0                            Artagaveytia, Mr. Ramon    male  71.0      0      0    PC 17609  49.5042   NaN        C  NaN  22.0      Montevideo, Uruguay
    ...      ...       ...                                                ...     ...   ...    ...    ...         ...      ...   ...      ...  ...   ...                      ...
    1293       3         0                  Williams, Mr. Howard Hugh "Harry"    male   NaN      0      0    A/5 2466   8.0500   NaN        S  NaN   NaN                      NaN
    1297       3         0                             Wiseman, Mr. Phillippe    male   NaN      0      0  A/4. 34244   7.2500   NaN        S  NaN   NaN                      NaN
    1302       3         0                                  Yousif, Mr. Wazli    male   NaN      0      0        2647   7.2250   NaN        C  NaN   NaN                      NaN
    1303       3         0                              Yousseff, Mr. Gerious    male   NaN      0      0        2627  14.4583   NaN        C  NaN   NaN                      NaN
    1305       3         0                              Zabour, Miss. Thamine  female   NaN      1      0        2665  14.4542   NaN        C  NaN   NaN                      NaN
    [1309 rows x 14 columns]
    ```

### NumPy Basics (`Numpy.ipynb`)

*   **NumPy version:**
    ```
    '1.19.2'
    ```
*   **Creating a 2D array:**
    ```
    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    ```
*   **Conditional element selection (`np.where`):**
    ```
    [[0 0 0]
     [0 0 6]
     [7 8 9]]
    ```
*   **Reshaping an array:**
    ```
    [[1 2]
     [3 4]
     [5 6]]
    ```
*   **Creating an array of ones:**
    ```
    [[1. 1.]
     [1. 1.]
     [1. 1.]]
    ```
*   **Creating an array of zeros:**
    ```
    [[0. 0. 0.]
     [0. 0. 0.]]
    ```
*   **Creating a full array:**
    ```
    [[5 5]
     [5 5]
     [5 5]]
    ```
*   **Creating an identity matrix:**
    ```
    [[1. 0. 0. 0.]
     [0. 1. 0. 0.]
     [0. 0. 1. 0.]
     [0. 0. 0. 1.]]
    ```
*   **Flipping an identity matrix:**
    ```
    [[0. 0. 0. 1.]
     [0. 0. 1. 0.]
     [0. 1. 0. 0.]
     [1. 0. 0. 0.]]
    ```
*   **Sorting an array:**
    ```
    array([1, 2, 3, 4, 5, 6, 7, 8])
    ```
*   **Concatenating arrays:**
    ```
    array([10, 20, 30, 40, 50, 60, 70, 80])
    ```
*   **Array sum:**
    ```
    100
    ```
*   **Array min/max:**
    ```
    10
    40
    ```

---
## Acknowledgements

This project was developed for educational and portfolio purposes, inspired by various online resources and documentation. The code has been rewritten and commented to demonstrate a thorough understanding of the concepts. All credit for the original educational materials and ideas goes to their respective creators.
---

# **Author:** mehran Asgari
## **Email:** [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com).
## **GitHub:** [https://github.com/imehranasgari](https://github.com/imehranasgari).

---

## 📄 License

This project is licensed under the MIT License – see the `LICENSE` file for details.