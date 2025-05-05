# Company Info Extractor with Groq API and yFinance

___

This project uses a powerful LLM from **Groq API** to extract structured information about companies, including their full names, stock tickers, nationalities, and current stock prices in both **USD** and **TRY**. The results are modeled using **Pydantic** and displayed as a **Pandas DataFrame**.

___

##  Features

- Input: Company names via natural language prompt
- Uses LLaMA 3.3 model via Groq API to interpret and extract company metadata
- Retrieves real-time stock data using **yfinance**
- Structured response using **Pydantic**
- Outputs data in a clean **Pandas DataFrame** format

___

## Technologies Used

- Python 3
- [Groq API](https://groq.com/)
- [yfinance](https://pypi.org/project/yfinance/)
- [Pydantic](https://docs.pydantic.dev/)
- [pandas](https://pandas.pydata.org/)
- [instructor](https://github.com/jxnl/instructor)

___

## How to Run

1. Clone this repository

```
https://github.com/berkyalkn/llm-company-info-agent
```

2. Install dependencies :

```
pip install -r requirements.txt
```

3. Set up your .env file with your Groq API key:

```
GROQ_API_KEY=your_key_here
```

___

## Example Output

Input :

    Give me structured information about the following companies: Mercadolibre and Meta.

Output :

|company_name |ticker | real_price(USD | real_price(TRY) | nationality |
| ------ | ----------- | ------------ | ---------- | ----------|
|Mercadolibre Inc.   | MELI | 2246.54 | 86648.60 | Argentine
|Meta Platforms Inc. | META | 599.27 | 23113.72 | American


## Security Note

Make sure to never commit your .env file. This is already added to .gitignore.


