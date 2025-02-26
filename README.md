# Projects Hub Backend

This is the backend service for the Projects Hub, a platform designed to manage and organize projects efficiently. It is built with TypeScript, utilizing Prisma for database management and PostgreSQL as the relational database.

## Prerequisites

Before you start, ensure that the following are installed on your machine:

- Node.js (v14 or later)
- PostgreSQL
- Prisma CLI

## Getting Started

### 1. Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/Oluwademiladeogo/projects-hub-backend.git
cd projects-hub-backend
```

### 2. Install Dependencies

Run the following command to install all the required dependencies:

```bash
npm install
```

### 3. Set Up the Environment Variables

Create a `.env` file in the root directory and add the following:

```env
DATABASE_URL="postgresql://<username>:<password>@localhost:5432/projectshub?schema=public"
```

Make sure to replace `<username>` and `<password>` with your PostgreSQL credentials.

> **Note:** Ensure the database URL is URL-encoded (e.g., `%20` for whitespaces).

### 4. Set Up the Database

To generate the Prisma client and migrate the database, run the following commands:

```bash
npx prisma generate
npx prisma migrate dev
```

This will set up the database and prepare it for use. If you make changes to the schema later, remember to run:

```bash
npx prisma migrate dev --name <version-name>
```

To update the schema when others make changes:

```bash
npx prisma dbPush
```

### 5. Run the Application

Once everything is set up, you can run the backend with:

```bash
npm start
```

Alternatively, for development, use:

```bash
npm run dev
```

This will start the application with live reload support.

## Project Structure

- `src/`: Contains all the backend logic.
- `package.json`: Manages project dependencies and scripts.
- `.env.example`: A sample environment configuration file.
- `prisma/`: Contains Prisma schema files and migrations.

## Technologies Used

- **TypeScript**: For building the backend application.
- **Prisma**: For database ORM (Object-Relational Mapping).
- **PostgreSQL**: Relational database for storing project data.
- **Express.js**: Web framework for handling HTTP requests.
  
## Contributing

If you'd like to contribute to this project, please fork the repository, make your changes, and submit a pull request. Ensure that your code follows the existing coding conventions and includes appropriate tests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
