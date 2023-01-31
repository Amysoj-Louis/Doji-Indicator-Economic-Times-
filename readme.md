# Doji Indicator (Economic Times)

This code extract stock symbols and stock types from [Economic Times](https://economictimes.indiatimes.com/). The code filters the data based on two predefined filters: `WHITE_SPINNING_TOP` and `BLACK_SPINNING_TOP`. The extracted data is then displayed using a Pandas DataFrame.

## Requirements

- Python 3
- Requests `pip install requests`
- Pandas `pip install pandas`

## Usage

- Clone the repository or download the code.
- Install the required packages (see Requirements).
- Run the code using python filename.py.
- The extracted data will be displayed in a Pandas DataFrame.

## API Endpoint

The API endpoint used in the code is:

```
https://etmarketsapis.indiatimes.com/ET_TechnicalScreeners/getFilteredData
```

## Payload

The code uses two different payloads for the two predefined filters. The payloads are as follows:

```
# Payload for filter 'WHITE SPINNING TOP'
payload = {
    'exchangeId': 50,  # Exchange ID
    'fieldNames': "symbol",  # Fields to retrieve
    'pageNumber': 1,  # Page number
    'pageSize': 1000,  # Page size
    'predefinedFilterName': "WHITE_SPINNING_TOP",  # Filter name
    'sortedField': "performanceD1",  # Sorting field
    'sortedOrder': "desc"  # Sorting order
}
```

```
# Payload for filter 'BLACK SPINNING TOP'
payload = {
    'exchangeId': 50,  # Exchange ID
    'fieldNames': "symbol",  # Fields to retrieve
    'pageNumber': 1,  # Page number
    'pageSize': 1000,  # Page size
    'predefinedFilterName': "BLACK_SPINNING_TOP",  # Filter name
    'sortedField': "performanceD1",  # Sorting field
    'sortedOrder': "desc"  # Sorting order
}
```

## Output

The extracted data is displayed in a Pandas DataFrame, with two columns: Symbol and Type. The Symbol column contains the stock symbols and the Type column contains the stock types (either WHITE SPINNING TOP or BLACK SPINNING TOP).

```
	Symbol	Type
0	CENTURYTEX	WHITE SPINNING TOP
1	MAZDOCK	WHITE SPINNING TOP
2	AIAENG	WHITE SPINNING TOP
3	ADANITRANS	WHITE SPINNING TOP
4	IDEA	WHITE SPINNING TOP
...	...	...
77	GLAXO	BLACK SPINNING TOP
78	360ONE	BLACK SPINNING TOP
79	KAJARIACER	BLACK SPINNING TOP
80	OIL	BLACK SPINNING TOP
81	TECHM	BLACK SPINNING TOP
```
