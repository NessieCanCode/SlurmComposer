# SlurmComposer

## Description
SlurmComposer is an intuitive web application designed to streamline the process of generating Slurm job submission scripts. By parsing Slurm configuration files, it provides a user-friendly interface to help users efficiently craft scripts, optimizing the use of available HPC resources.

## Features
- Parse Slurm configuration files to extract cluster details
- Interactive UI for crafting Slurm job submission scripts
- Support for various node types and partition configurations
- Exportable script generation for immediate use
- User authentication and saved configurations (TBD)

## Tech Stack
- Frontend: React.js / Vue.js with Tailwind CSS / Bootstrap
- Backend: Node.js with Express.js
- Database: MongoDB / PostgreSQL
- DevOps: Docker, GitHub Actions for CI/CD

## Installation

### Prerequisites
- Node.js (LTS version)
- Yarn or npm (Node.js package manager)
- Docker (optional, for containerization)
- MongoDB or PostgreSQL (depending on your choice)

### Cloning the Repository
\```bash
git clone https://github.com/yourusername/SlurmComposer.git
cd SlurmComposer
\```

### Frontend Setup
\```bash
cd frontend
yarn install # or npm install
yarn start # or npm start
\```
This will start the development server for the frontend. Navigate to `http://localhost:3000` to view it in the browser.

### Backend Setup
\```bash
cd backend
yarn install # or npm install
yarn dev # or npm run dev
\```
This will start the backend server, which by default will run on `http://localhost:5000`.

### Environment Variables
Set up the necessary environment variables in a `.env` file at the root of your backend project:

\```env
DATABASE_URL=mongodb://localhost/slurmcomposer
SESSION_SECRET=your-session-secret
\```

Replace `mongodb://localhost/slurmcomposer` with your database connection string.

### Running Tests
To run the test suite:

\```bash
cd backend
yarn test # or npm test
\```

### Docker (Optional)
To containerize SlurmComposer, use the provided `Dockerfile` and `docker-compose.yml`.

\```bash
docker-compose up --build
\```

This command builds the images and starts the containers defined in `docker-compose.yml`.

## Deployment

For deployment, you can use services like Heroku, DigitalOcean, AWS, or any other cloud provider.

### Heroku Deployment
\```bash
heroku create slurmcomposer
git push heroku main
heroku open
\```

### DigitalOcean Deployment
DigitalOcean offers an App Platform that can automatically deploy from your repository.

### AWS Deployment
AWS has several options for deployment, including Elastic Beanstalk, ECS, and EKS.

## Contributing
We welcome contributions! Please read `CONTRIBUTING.md` for details on our code of conduct and the process for submitting pull requests.

## License
This project is licensed under the GNU General Public License version 3 - see the `LICENSE` file for details.

## Acknowledgments
- Slurm Project
- Contributors and maintainers of the used open-source packages


