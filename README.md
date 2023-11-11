# SlurmCostManager

## Description
SlurmCostManager is a comprehensive web application designed to facilitate the accounting and billing of HPC resources in Slurm-managed environments. This tool simplifies the process of tracking resource usage and calculating costs, providing research institutions with a robust and user-friendly interface for managing their HPC expenditures.

## Project Structure

Below is an outline of the folder structure for SlurmCostManager:

```
SlurmComposer/
│
├── frontend/             # Frontend part of the project
│   ├── public/           # Static files
│   ├── src/              # React/Vue source files
│   │   ├── components/   # UI components
│   │   ├── views/        # Pages
│   │   ├── app/          # App setup and main files
│   │   ├── utils/        # Utility functions
│   │   ├── store/        # State management (Redux/Vuex store)
│   │   └── styles/       # CSS/SCSS/Tailwind files
│   ├── .env              # Environment variables for the frontend
│   ├── package.json      # Frontend dependencies and scripts
│   └── ...
│
├── backend/              # Backend part of the project
│   ├── src/              # Backend source files
│   │   ├── controllers/  # Request handlers
│   │   ├── models/       # Database models
│   │   ├── routes/       # Routes definitions
│   │   ├── middleware/   # Custom middleware
│   │   └── app.js        # Express app setup
│   ├── .env              # Environment variables for the backend
│   ├── package.json      # Backend dependencies and scripts
│   └── ...
│
├── config/               # Configuration files for various environments
│   ├── default.json      # Default config
│   ├── production.json   # Production-specific config
│   └── ...
│
├── scripts/              # Utility scripts (e.g., setup and deployment scripts)
│
├── test/                 # Test suite files
│   ├── frontend/         # Frontend test files
│   └── backend/          # Backend test files
│
├── .github/              # GitHub configuration files (e.g., workflows for actions)
│   └── workflows/        # CI/CD workflow definitions
│
├── .gitignore            # Specifies intentionally untracked files to ignore
├── README.md             # Project overview documentation
├── CONTRIBUTING.md       # Contribution guidelines
├── LICENSE               # The license file
└── docker-compose.yml    # Docker compose file (if using Docker)
```

Each directory has a specific role:

- `frontend/`: Contains all the source code for the application's user interface.
- `backend/`: Houses the server-side code, including APIs, business logic, and database models.
- `config/`: Configuration settings for different deployment environments.
- `scripts/`: Includes scripts for database migration, deployment, and other utilities.
- `test/`: Test code to ensure the application runs as expected.
- `.github/`: Configuration for GitHub-specific features like Actions for CI/CD.
- `.gitignore`: File specifying the untracked files that Git should ignore.
- `README.md`: The main documentation file for the project, detailing setup, usage, etc.
- `CONTRIBUTING.md`: Instructions and guidelines for contributors.
- `LICENSE`: The legal license agreement for the project.
- `docker-compose.yml`: Docker compose configuration for container orchestration (optional).



## Features
- Seamless integration with Slurm for real-time data fetching
- Intuitive UI for monitoring and managing HPC resource usage
- Detailed cost calculation based on user-defined parameters
- Automated invoice generation for resource usage
- Detailed reports and analytics for usage insights
- Secure user authentication and role-based access control

## Tech Stack
- Frontend: React.js / Vue.js with Tailwind CSS / Bootstrap
- Backend: Node.js with Express.js
- Database: MongoDB / PostgreSQL for storing usage and billing data
- DevOps: Docker, GitHub Actions for CI/CD

## Installation

### Prerequisites
- Node.js (LTS version)
- Yarn or npm (Node.js package manager)
- Docker (optional, for containerization)
- MongoDB or PostgreSQL (depending on your choice)

### Cloning the Repository
git clone https://github.com/yourusername/SlurmComposer.git
cd SlurmComposer


### Frontend Setup
cd frontend
yarn install # or npm install
yarn start # or npm start

This will start the development server for the frontend. Navigate to `http://localhost:3000` to view it in the browser.

### Backend Setup
cd backend
yarn install # or npm install
yarn dev # or npm run dev

This will start the backend server, which will run on `http://localhost:5000` by default.

### Environment Variables
Set up the necessary environment variables in a `.env` file at the root of your backend project:

DATABASE_URL=mongodb://localhost/slurmcomposer
SESSION_SECRET=your-session-secret


Replace `mongodb://localhost/SlurmCostManager` with your database connection string.

### Running Tests
To run the test suite:

cd backend
yarn test # or npm test


### Docker (Optional)
To containerize SlurmComposer, use the provided `Dockerfile` and `docker-compose.yml`.

docker-compose up --build


This command builds the images and starts the containers defined in `docker-compose.yml`.

## Deployment

You can use services like Heroku, DigitalOcean, AWS, or any other cloud provider for deployment.

### Heroku Deployment
heroku create SlurmCostManager
git push heroku main
heroku open


### DigitalOcean Deployment
DigitalOcean offers an App Platform that can automatically deploy from your repository.

### AWS Deployment
AWS has several options for deployment, including Elastic Beanstalk, ECS, and EKS.

## Contributing
We welcome contributions! Please read `CONTRIBUTING.md` for details on our code of conduct and the process for submitting pull requests.

## License
This project is licensed under the GNU General Public License version 3 - see the `LICENSE` file for details.

## Acknowledgments
- Slurm Project for providing the base HPC management system.
- Contributors and maintainers of the used open-source packages.


