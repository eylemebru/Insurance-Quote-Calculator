# Insurance Quote Calculator

A web application built with ASP.NET Core MVC that calculates insurance quotes based on various user inputs and risk factors.

## Features

- Calculate insurance quotes based on:
  - Age of the insured person
  - Car details (year, make, model)
  - Driving history (speeding tickets, DUI)
  - Coverage type (basic/full coverage)
- Admin panel to view all quotes
- Responsive design
- Data persistence using SQLite database

## Calculation Rules

The quote is calculated based on the following rules:

1. Base quote: $50/month
2. Age-based additions:
   - 18 or under: +$100
   - 19-25: +$50
   - 26 or older: +$25
3. Car-based additions:
   - Pre-2000 car: +$25
   - Post-2015 car: +$25
   - Porsche: +$25
   - Porsche 911 Carrera: +additional $25
4. Risk factors:
   - Each speeding ticket: +$10
   - DUI history: +25% to total
   - Full coverage: +50% to total

## Technical Details

- **Framework**: ASP.NET Core MVC (.NET 8.0)
- **Database**: SQLite
- **ORM**: Entity Framework Core
- **Frontend**: Bootstrap 5
- **Validation**: Data Annotations

## Getting Started

### Prerequisites

- .NET 8.0 SDK
- Visual Studio 2022 or VS Code

### Installation

1. Clone the repository:
```bash
git clone [repository-url]
```

2. Navigate to the project directory:
```bash
cd InsuranceQuoteCalculator.Web
```

3. Restore dependencies:
```bash
dotnet restore
```

4. Run database migrations:
```bash
dotnet ef database update
```

5. Run the application:
```bash
dotnet run
```

The application will be available at `http://localhost:5167`

## Project Structure

- `Models/`: Contains the Insuree model with validation rules
- `Controllers/`: Contains the InsureeController with quote calculation logic
- `Views/`: Contains all views (Create, Index, Admin)
- `Data/`: Contains DbContext and database configuration

## Usage

1. Navigate to "Get Quote" to create a new insurance quote
2. Fill in all required information
3. Submit the form to get your quote
4. View all quotes in the "Quotes" section
5. Access detailed information in the "Admin" section

