---
icon: hand-wave
---

# Start with AllDefi

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

##
