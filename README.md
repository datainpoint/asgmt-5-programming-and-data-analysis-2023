# asgmt-5-programming-and-data-analysis-2023

> Assignment 5: Programming and Data Analysis 2023.

Define functions or classes in `asgmt-five.py` with given names and templates then run `test-runner.py`.

## 01. Define a class `SquareSqrtArgs` which instantiates objects with two methods `square_args()` and `sqrt_args()` that take flexible integers and returns their squared and square-root values in a `list`.

```python
class SquareSqrtArgs:
    """
    >>> square_sqrt_args = SquareSqrtArgs()
    >>> square_sqrt_args.square_args(0, 1, 2)
    [0, 1, 4]
    >>> square_sqrt_args.sqrt_args(0, 1, 4)
    [0.0, 1.0, 2.0]
    >>> square_sqrt_args.square_args(3, 4, 5)
    [9, 16, 25]
    >>> square_sqrt_args.sqrt_args(9, 16, 25)
    [3.0, 4.0, 5.0]
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```

## 02. Define a class `Palindrome` which instantiates objects with 2 attributes `original_text` and `reversed_text`, and 1 method `is_palindrome()`.

Source: <https://en.wikipedia.org/wiki/Palindrome>

```python
class Palindrome:
    """
    >>> palindrome = Palindrome('eye')
    >>> palindrome.original_text
    'eye'
    >>> palindrome.reversed_text
    'eye'
    >>> palindrome.is_palindrome()
    True
    >>> palindrome = Palindrome('dye')
    >>> palindrome.original_text
    'dye'
    >>> palindrome.reversed_text
    'eyd'
    >>> palindrome.is_palindrome()
    False
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```

## 03. Define a class `CommonDivisors` which instantiates objects with 2 attributes `x_divisors` and `y_divisors`, and 1 method `get_common_divisors()`.

```python
class CommonDivisors:
    """
    >>> cd = CommonDivisors(3, 6)
    >>> cd.x_divisors
    {1, 3}
    >>> cd.y_divisors
    {1, 2, 3, 6}
    >>> cd.get_common_divisors()
    {1, 3}
    >>> cd = CommonDivisors(4, 8)
    >>> cd.x_divisors
    {1, 2, 4}
    >>> cd.y_divisors
    {1, 2, 4, 8}
    >>> cd.get_common_divisors()
    {1, 2, 4}
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```

## 04. Define a class `PrimeJudger` which instantiates objects with 2 methods `get_divisors()`, `is_prime()`.

```python
class PrimeJudger:
    """
    >>> pj = PrimeJudger(1)
    >>> pj.get_divisors()
    {1}
    >>> pj.is_prime()
    False
    >>> pj = PrimeJudger(2)
    >>> pj.get_divisors()
    {1, 2}
    >>> pj.is_prime()
    True
    >>> pj = PrimeJudger(4)
    >>> pj.get_divisors()
    {1, 2, 4}
    >>> pj.is_prime()
    False
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```

## 05. Define a function `import_countries_json` which imports the `countries.json` as a `list` in working directory.

```python
def import_countries_json() -> list:
    """
    >>> countries_json = import_countries_json()
    >>> type(countries_json)
    list
    >>> len(countries_json)
    249
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```

## 06. Define a function `lookup_country_iso_codes` which returns the 2-digit and 3-digit ISO country code given the name of country, based on `countries.json` in working directory.

```python
def lookup_country_iso_codes(country: str) -> tuple:
    """
    >>> lookup_country_iso_codes("Taiwan")
    ('TW', 'TWN')
    >>> lookup_country_iso_codes("Japan")
    ('JP', 'JPN')
    >>> lookup_country_iso_codes("Lithuania")
    ('LT', 'LTU')
    >>> lookup_country_iso_codes("Slovenia")
    ('SI', 'SVN')
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```

## 07. Define a function `import_movies_csv()` which creates a DataFrame of IMDb's top 250 rated movies of all time given `movies.csv` in working directory.

```python
def import_movies_csv() -> pd.core.frame.DataFrame:
    """
    >>> movies = import_movies_csv()
    >>> type(movies)
    pandas.core.frame.DataFrame
    >>> movies.shape
    (250, 6)
    """
    ### BEGIN SOLUTION

    ### END SOLUTION
```

## 08. Define a class `DataframeAttrs` which instantiates objects with 3 methods `get_shape()`, `get_dtypes()`, and `get_summary()`.

```python
class DataframeAttrs:
    """
    >>> movies = import_movies_csv()
    >>> dfa = DataframeAttrs(movies)
    >>> dfa.get_shape()
    (250, 6)
    >>> dfa.get_dtypes()
    id                int64
    title            object
    release_year      int64
    runtime           int64
    rating          float64
    link             object
    dtype: object
    >>> dfa.get_summary()
                   id  release_year     runtime      rating
    count  250.000000    250.000000  250.000000  250.000000
    mean   125.500000   1986.816000  129.052000    8.309600
    std     72.312977     25.387086   29.916505    0.234538
    min      1.000000   1921.000000   45.000000    8.000000
    25%     63.250000   1966.250000  107.250000    8.100000
    50%    125.500000   1994.500000  126.500000    8.200000
    75%    187.750000   2007.000000  145.750000    8.400000
    max    250.000000   2023.000000  238.000000    9.300000
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```

## 09. Define a function `find_top_gun_maverick()` which finds out "Top Gun: Maverick" given `movies.csv` in working directory.

```python
def find_top_gun_maverick() -> pd.core.frame.DataFrame:
    """
    >>> top_gun_maverick = find_top_gun_maverick()
    >>> type(top_gun_maverick)
    pandas.core.frame.DataFrame
    >>> top_gun_maverick.shape
    (1, 6)
    >>> print(top_gun_maverick)
          id              title  release_year  runtime  rating                                    link
    126  127  Top Gun: Maverick          2022      130     8.3  https://www.imdb.com//title/tt1745960/
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```

## 10. Define a function `find_starwars_episodes()` which finds out "Star Wars" episodes given `movies.csv` in working directory.

```python
def find_starwars_episodes() -> pd.core.frame.DataFrame:
    """
    >>> starwars_episodes = find_starwars_episodes()
    >>> type(starwars_episodes)
    pandas.core.frame.DataFrame
    >>> starwars_episodes.shape
    (3, 6)
    >>> print(starwars_episodes)
        id                                           title  release_year  runtime  rating                                    link
    15  16  Star Wars: Episode V - The Empire Strikes Back          1980      124     8.7  https://www.imdb.com//title/tt0080684/
    29  30              Star Wars: Episode IV - A New Hope          1977      121     8.6  https://www.imdb.com//title/tt0076759/
    91  92      Star Wars: Episode VI - Return of the Jedi          1983      131     8.3  https://www.imdb.com//title/tt0086190/
    """
    ### BEGIN SOLUTION
    
    ### END SOLUTION
```