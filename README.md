# Rythu Direct: 
# Direct Farmer Marketplace & APMC Mandi Network
Rythu Direct connects farmers to wholesale buyers in Andhra Pradesh. Farmers add details of what they want to sell at a set price. Buyers use this data to negotiate better rates than the mandi. There is also an ML-powered suggestion module that recommends a fair price. The app was built with Node.js and Express, SQLite, and JavaScript.

Rythu Direct is a web application that connects farmers directly with wholesale buyers. 
Farmers can register, list their produce, and see live mandi (APMC market) rates, so they can sell at fair prices without depending entirely on middlemen. 
The project covers the Farmer, Crop and Market relationship across districts in Andhra Pradesh.

# https://rythu-direct-app.ai.studio => Live Demo

## Features

- **Farmer registration and login**: farmers create an account and manage their profile.
- **Produce listings**: farmers add crops with quantity, price and location.
- **Buyer browsing**: wholesale buyers search listings by crop and district.
- **Live mandi rates**: current APMC market prices for comparison.
- **Crop and market linking**: each crop is connected to the markets where it sells.
- **ML price insights** *(if included)*: a Python model that gives a rough price prediction for crops.

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Node.js, Express |
| Database | SQLite |
| ML module | Python (scikit-learn / pandas) |

## Project Structure

```
rythu-direct-app/
├── public/          # Frontend pages (HTML, CSS, JS)
├── server/          # Node.js backend and API routes
├── database/        # SQLite database file and schema
├── ml/              # Python model and prediction scripts
├── package.json
└── README.md
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- [Python](https://www.python.org/) (3.9 or later), for the ML module
- Git

### 1. Clone the repository

```bash
git clone [your-repo-url]
cd rythu-direct-app
```

### 2. Install backend dependencies

```bash
npm install
```

### 3. Set up the database

```bash
npm run setup-db
```

This creates the SQLite database and tables. [Adjust this command to match your project.]

### 4. (Optional) Set up the ML module

```bash
cd ml
pip install -r requirements.txt
python train_model.py
cd ..
```

### 5. Run the app
```bash
npm start
```

Then open **http://localhost:3000** in your browser. [Change the port if your project uses a different one.]

## How to Use
1. **Register** as a farmer or buyer from the sign-up page.
2. **Log in** with your credentials.
3. **Farmers:** add a crop listing with the crop name, quantity, expected price and district.
4. **Buyers:** search listings by crop or district and contact the farmer.
5. **Check mandi rates** on the market page before you sell or buy.

## Workflow
1. Farmer registers and logs in.
2. Farmer adds a crop listing linked to a district and market.
3. Buyer searches for crops and sees the listing along with the live mandi rate.
4. Buyer contacts the farmer and the deal is made directly, with no middleman.

## API Overview
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/register` | Register a new farmer or buyer |
| POST | `/api/login` | Log in |
| GET | `/api/crops` | List all crop listings |
| POST | `/api/crops` | Add a new crop listing |
| GET | `/api/markets` | Get mandi market rates |

[Update this table to match your actual routes.]

## Future Scope
- Mobile app for farmers in local languages (Telugu and English)
- SMS alerts for price changes
- Payment integration
- Better price prediction with more historical data

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

## License
This project is licensed under the [MIT License](LICENSE).
Made with ❤️ for farmers of Andhra Pradesh.
