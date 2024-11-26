---
icon: hand-wave
---

# ALLDEFI Project Documentation

This documentation provides a comprehensive overview of the ALLDEFI project, including its purpose, installation instructions, structure, functionality, usage, and additional resources. The aim is to facilitate understanding and contribution to the project.

## **1. Introduction**

**1.1 Purpose of the Project**

**ALLDEFI** was founded by technology, security, and crypto enthusiasts who believe decentralized finance (DeFi) should be safe and easy to navigate. The mission of ALLDEFI is to make DeFi accessible to all by providing better passive income opportunities than what is currently available in the markets.

DeFi offers a great way to earn passive income, but there are two significant problems:

• **User Experience**: Navigating DeFi platforms is clunky and time-consuming, even for seasoned crypto investors. Users typically have to set up wallets, secure recovery passphrases, acquire specific crypto assets, swap, bridge across blockchains, and sign multiple transaction messages.

• **Security Concerns**: DeFi attracts increasingly sophisticated scams, frauds, and hacks. Researching the most trustworthy DeFi protocols can be overwhelming for any investor.

**1.2 How ALLDEFI Works**

ALLDEFI has researched and audited thousands of DeFi protocols across 20 criteria. The platform handles the cumbersome DeFi steps so users don’t have to. The result is a varied selection of trustworthy DeFi products for investing without friction.

Key aspects of how ALLDEFI operates:

• **Simplified Investing**: Users can invest in DeFi products without dealing with the technical complexities.

• **Continuous Auditing**: ALLDEFI continuously audits new DeFi products to provide access to the latest and most trusted passive income opportunities.

• **User-Friendly Interface**: The platform offers an intuitive interface for managing investments and withdrawals.

**1.3 Credentials**

ALLDEFI’s founding team comes from the cybersecurity industry, embedding security principles into the corporate culture. Client funds are held in a bank account and are never commingled or used for anything other than the clients’ investment selections.

• **Regulatory Compliance**: Registered with Banco de España, Spain’s central bank, as a provider of services of exchange of virtual currency for fiat currency and custody of electronic wallets.

• **Security Infrastructure**: Securely manages cryptocurrency funds using multi-party computation (MPC), one of the most secure architectures available.

• **Certifications**: Infrastructure partnership is certified to SOC 2 Type 2 and ISO standards for cloud, security, and privacy.

**1.4 Technologies Used**

• **Backend**: Laravel Framework (Version 10.x)

• **Frontend**: Vue.js (Version 2.x), Tailwind CSS

• **Backoffice**: Backpack for Laravel

• **Authentication and Security**: Laravel Jetstream, Laravel Fortify

• **Database**: MySQL or compatible relational database

• **Server Environment**: Linux-based systems

• **Additional Tools and Packages**:

• **Fireblocks SDK**: For secure crypto transactions

• **CoinGecko API**: Cryptocurrency market data

• **Covalent API**: Blockchain data

• **MailerLite**: Email marketing automation

• **AWS S3**: Storage solution

• **Swagger**: API documentation

• **Chart.js and ApexCharts**: Data visualization

• **Laravel Sanctum**: API authentication

• **Spatie Query Builder**: For API query customization

## **2. Installation Guide**

**2.1 Prerequisites**

Ensure that you have the following software installed on your system:

`•`` `**`Operating System`**`: Linux distribution (e.g., Ubuntu, Debian, CentOS)`

`•`` `**`PHP`**`: Version 8.1 or higher`

`•`` `**`Composer`**`: Latest version`

`•`` `**`Node.js`**`: Version 14.x or higher`

`•`` `**`npm`**`: Comes with Node.js`

`•`` `**`MySQL`**`: Version 5.7 or higher`

`•`` `**`Git`**`: For cloning the repository`

• **Additional PHP Extensions**:

• mbstring, openssl, pdo, tokenizer, xml, ctype, json, bcmath, curl, gd, fileinfo, intl, exif

**2.2 Installation Steps**

**1. Clone the Repository**

`git clone https://github.com/your-username/ALLDEFI.git`

`cd ALLDEFI`

_Replace_ _your-username_ _with your GitHub username._

**2. Configure Environment Variables**

Copy the example environment file and generate an application key:

`cp .env.example .env`

`php artisan key:generate`

**3. Set Up the Database**

Edit the .env file to configure your database connection:

`DB_CONNECTION=mysql`

`DB_HOST=127.0.0.1`

`DB_PORT=3306`

`DB_DATABASE=alldefi_db`

`DB_USERNAME=your_db_username`

`DB_PASSWORD=your_db_password`

_Replace_ _your\_db\_username_ _and_ _your\_db\_password_ _with your database credentials._

**4. Install PHP Dependencies**

`composer install`

**5. Install JavaScript Dependencies**

`npm install`

**6. Compile Frontend Assets**

For development:

`npm run dev`

For production:

`npm run prod`

**7. Run Database Migrations and Seeders**

`php artisan migrate --seed`

_Ensure that seeders do not include data from_ _Adminold_ _or_ _Deleteme_ _directories._

**8. Set Up Storage Link**

`php artisan storage:link`

**9. Configure Additional Services**

• **AWS S3**: Set up AWS credentials in .env if using S3 storage.

• **MailerLite**: Add MailerLite API key to .env.

• **Fireblocks SDK**: Configure API credentials in .env.

**10. Start the Development Server**

php artisan serve

Visit http://localhost:8000 in your web browser to access the application.

## **3. Project Structure**

**3.1 Directory Overview**

The project follows the standard Laravel application structure with custom directories for specific functionalities.

ALLDEFI/

├── app/

│ ├── Console/

│ ├── Exceptions/

│ ├── Helpers/ # Custom helper functions

│ ├── Http/

│ │ ├── Controllers/

│ │ │ ├── Admin/ # Backoffice controllers (to document)

│ │ │ ├── Auth/

│ │ │ ├── API/

│ │ │ ├── ...

│ │ ├── Middleware/

│ │ └── Requests/

│ ├── Models/

│ ├── Observers/

│ ├── Providers/

│ └── Services/ # External service integrations

├── bootstrap/

├── config/

├── database/

│ ├── factories/

│ ├── migrations/

│ └── seeders/

├── public/

├── resources/

│ ├── js/

│ │ ├── components/ # Vue.js components

│ │ ├── pages/ # Vue.js pages

│ │ ├── app.js

│ │ └── ...

│ ├── lang/

│ ├── sass/

│ └── views/

├── routes/

│ ├── web.php # Web routes

│ ├── api.php # API routes

│ ├── admin.php # Admin routes

│ └── ...

├── storage/

├── tests/

├── vendor/

├── composer.json

├── package.json

└── .env

**Important Directories and Files:**

• **app/Http/Controllers/Admin/**: Contains Backpack admin panel controllers.

• **app/Http/Controllers/Adminold/**: Deprecated admin controllers (not documented).

• **app/Deleteme/**: Files marked for deletion (not documented).

• **resources/js/**: Contains Vue.js frontend code.

• **config/**: Configuration files for packages and services.

• **routes/admin.php**: Routes specific to the admin panel.

## **4. System Functionality**

**4.1 User Functionalities**

• **Registration and Login**: Users can create an account by providing their personal information and secure credentials. Once registered, they can log in to the system to access its features.

• **KYC (Know Your Customer)**: Identity verification process where users must provide documents and personal data to comply with legal regulations and internal security policies.

• **Cryptocurrency Deposit**: Users can deposit supported cryptocurrencies into their accounts, which will be reflected in their balance and available for investment.

• **FIAT Currency Deposit**: Ability to deposit fiat currency (e.g., USD, EUR) through bank transfers or other payment methods accepted by the platform.

• **Investment in Products**: Users can invest in different financial products offered by the platform, adjusting amounts and selecting products according to their profile and preferences.

• **Disinvestment from Products**: Option to withdraw investments from specific products, allowing users to liquidate positions and obtain their funds.

• **Withdrawals**: Users can request the withdrawal of available funds in their account, whether in cryptocurrencies or fiat currency, following established procedures.

**4.2 Administration Functionalities**

• **Product Management**: Administrators can create, modify, and delete financial products available for investment, setting characteristics such as interest rates, terms, and conditions.

• **Portfolio Management**: Administration of investment portfolios, including asset allocation, performance tracking, and strategic adjustments according to market conditions.

• **Updating Product and Currency Information**: Maintenance and updating of relevant data about the offered products and accepted currencies, ensuring accurate information for users.

• **Referral System**: Implementation and management of a referral program that incentivizes users to invite new clients, establishing rewards and tracking referrals.

• **Benefit Payment Management**: Control and processing of payments corresponding to the benefits generated by users’ investments, ensuring accurate and timely transactions.

• **Commission (Fees) Management System**: Configuration and administration of commissions applied to transactions, deposits, withdrawals, and other services, allowing adjustments according to internal policies.

• **Customer Risk Management**: Continuous evaluation of the risk associated with clients, implementing measures such as investment limits, alerts, and monitoring of suspicious activities.

• **Product Audit and Valuation**: Periodic audits on financial products, evaluating their performance, regulatory compliance, and conducting updated valuations for decision-making.

**4.3 Diagrams**

TBD _(Placeholder for including diagrams in PNG format.)_

## **5. Code Guide**

**5.1 Source Info**

**Backend**

Esta sección contiene la documentación generada automáticamente para el backend de Laravel. Haz clic en las secciones a continuación para explorar los detalles.

[Ver documentación completa](index.html)

**Frontend**

Esta sección contiene la guía de estilo de los componentes Vue2 generada con Styleguidist.

[Ver guía completa](index.html)

**API**

Esta sección contiene la documentación de los endpoints de la API generada con Swagger.

[Abrir documentación interactiva](index.html)

**5.2 Routes**

User:

* routes/web.php
* app/Http/Controllers/
* resources/js/Pages/
* app/Models

Admin:

* routes/web\_admin.php
* app/Http/Controllers/AdminOld/
* resources/js/Pages/AdminOld
* app/Models

**532 Coding Standards**

• **PHP**: Follow PSR-12 standards.

• **JavaScript**: Use ES6 syntax and Vue.js best practices.

• **CSS**: Utilize Tailwind CSS conventions.

• **Documentation**: Keep comments and documentation up-to-date.
