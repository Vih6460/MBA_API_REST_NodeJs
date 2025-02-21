# First API REST with NodeJs

This project is focused on developing a robust and efficient REST API using Fastify, Knex, and TypeScript. It aims to deepen the understanding of core backend concepts in Node.js, exploring how key functionalities work under the hood. The API implementation includes features such as middleware handling, database interactions with Knex, efficient request processing using Fastify, and support for file storage. Additionally, the project incorporates automated tests to ensure reliability and uses migrations for managing the local database schema.

## Features

- Middleware implementation
- Migrations for database
- User management:
  - Create a new transaction
  - List all transactions
  - List specific transactions
  - List summary
- Data persistence using local file storage
- Session id saved in cookies

## Getting Started

### Prerequisites

Ensure you have Node.js installed on your system. You can download it from [Node.js official website](https://nodejs.org/).

### Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/Vih6460/MBA_API_REST_NodeJs.git
   ```
2. Navigate to the project directory:
   ```sh
   cd MBA_API_REST_NodeJs/
   ```
2. Install the dependencies:
   ```sh
   npm i
   ```

### Usage

To start the server, run:
```sh
npm run dev
```
The server will be running on `http://localhost:3333`. You can change it on file 'src/server.js'

To stop the server, press `CTRL + C` in the terminal.

### API Endpoints

#### Create a transaction
```http
POST /transactions
```
Creates a new transaction. Requires a JSON body with transaction details.
```json
{
    "title": "Job",
    "amount": 300,
 	"type": "credit"
}
```

#### List all transactions
```http
GET /transactions
```
Retrieves a list of all transactions stored in the local database.

#### List especific transactions
```http
GET /transactions/:id
```
Retrieves the transaction who match with the id

#### List summary
```http
GET /transactions/summary
```
Retrieves the amount of your transactinons

## Contributing

Feel free to fork this repository and submit pull requests with improvements or additional features.

## License

This project is licensed under the MIT License.

---

Happy coding! 🚀
