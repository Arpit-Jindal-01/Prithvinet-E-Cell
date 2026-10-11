# PrithviNet | Environmental Intelligence Platform

PrithviNet is an environmental monitoring and community-response platform designed to help citizens and environmental authorities understand local environmental conditions, monitor pollution indicators, and coordinate responses to environmental concerns.

The platform is organized around four user roles: **Citizen, Regional Officer, Officer, and Head Administrator**. Each role is intended to provide a different view of environmental information and reporting workflows.

> **Project status:** Academic/project prototype. The repository includes a React + Vite frontend and supporting API/backend directories. Actual sensor connectivity, prediction-model performance, and deployment integrations should be verified against the running environment before being described as production capabilities.

## Problem

Environmental data can be difficult for residents and local authorities to access, interpret, and act on in one place. Pollution concerns may also require coordination between citizens, local committees, regional officers, and administrators.

PrithviNet aims to bring environmental indicators, regional visibility, and community reporting into a unified interface.

## Solution

PrithviNet provides a centralized environmental intelligence interface for viewing environmental indicators, exploring information by geographic region, and reporting environmental issues. The intended system can display measurements such as SO₂ and oxygen levels, support pollution-level forecasting, and help route community reports to the relevant authorities.

The reliability of displayed measurements and forecasts depends on the data sources and model integrations configured for a deployment.

## User Roles

### Citizen
- View environmental information relevant to their surroundings.
- Explore nearby regions and community resources.
- Submit reports about pollution, waste, or other environmental concerns.
- Find or connect with nearby committees for community coordination during environmental incidents or emergencies.

### Regional Officer
- View environmental information scoped to their assigned region.
- Review reports submitted by citizens in the region.
- Monitor local environmental concerns and coordinate follow-up actions.

### Officer
- Access environmental monitoring and reporting workflows according to the permissions assigned to the role.
- Review relevant environmental information and support operational response.

### Head Administrator
- Access a broader, system-wide view of environmental information.
- Oversee regional activity and review reports across regions.
- Monitor regional operations and platform activity.

> Role names and permission boundaries should match the authorization rules implemented in the current application. Do not rely on frontend-only hiding of pages as an access-control mechanism.

## Core Features

- **Environmental indicators:** Interface for viewing measurements such as SO₂ and oxygen levels, with support for additional environmental indicators.
- **Regional map view:** Geographic exploration of environmental information and region-specific views.
- **Role-oriented dashboards:** Different views for citizens, regional officers, officers, and the head administrator.
- **Pollution forecasting:** A place for displaying predicted pollution levels when a prediction model and suitable data source are configured.
- **Citizen reporting:** Submit environmental concerns for review by the appropriate regional team or administrator.
- **Community coordination:** Discover or connect with nearby committees for local environmental action and emergency coordination.
- **Administrative oversight:** Provide a consolidated view of regional activity and submitted reports.

## Technology Stack

The repository's `package.json` identifies the following frontend technologies and libraries:

- **React 18** for the user interface.
- **Vite 6** for development and production builds.
- **React Router** for client-side navigation.
- **Material UI** and **Radix UI** components for interface elements.
- **Tailwind CSS 4** for utility-based styling.
- **Recharts** for charts and data visualizations.
- **Lucide React** for icons.
- **jsPDF** and **jsPDF-AutoTable** for PDF/table export functionality where used.

The repository also contains `api/`, `backend/`, and `netlify/functions/` directories. Their runtime responsibilities and dependencies should be confirmed from those directories before documenting a specific backend framework, database, sensor protocol, or machine-learning library.

## Repository Structure

```text
Prithvinet-E-Cell/
├── api/                  # API-related code
├── backend/              # Backend services
├── guidelines/           # Project guidelines and supporting material
├── netlify/functions/    # Netlify serverless functions
├── public/               # Static assets
├── src/                  # React application source
├── .env.example          # Example environment configuration
├── netlify.toml          # Netlify configuration
├── render.yaml           # Render deployment configuration
├── vercel.json           # Vercel configuration
├── vite.config.ts        # Vite configuration
└── package.json          # Scripts and frontend dependencies
```

## Getting Started

### Prerequisites
- Node.js compatible with the installed Vite version.
- npm.
- Git.

### Install dependencies

```bash
git clone https://github.com/Arpit-Jindal-01/Prithvinet-E-Cell.git
cd Prithvinet-E-Cell
npm install
```

### Run the frontend locally

```bash
npm run dev
```

Vite will print the local development URL in the terminal, usually `http://localhost:5173`.

### Create a production build

```bash
npm run build
```

Follow any additional setup instructions required by the `backend/`, `api/`, or `netlify/functions/` code if those services are needed for the features you want to test.

## Configuration

An `.env.example` file is included in the repository. Review it before running services that depend on external APIs or environment variables.

1. Copy the example to the appropriate local environment file required by the project.
2. Fill in required values using your own development credentials.
3. Never commit secrets, private API keys, or production credentials.
4. Keep frontend-exposed environment variables free of secrets because client-side values can be visible to users.

The exact variable names and required services should be taken from `.env.example` and the relevant source files.

## Example Workflows

### Report an environmental issue
1. A citizen opens the reporting interface.
2. The citizen submits the environmental concern and its location.
3. The report is made available to the responsible regional team or administrator.
4. The relevant authority reviews the report and coordinates a response.

### Review regional environmental conditions
1. A regional officer opens their regional dashboard.
2. The officer views environmental indicators and reports for the assigned area.
3. The officer identifies issues that may require investigation or follow-up.

### System-wide oversight
1. The head administrator opens the administrative dashboard.
2. The administrator reviews information across regions and regional activity.
3. The administrator identifies reports or areas that need attention.

These workflows describe the intended product behavior. Verify that each step is implemented and connected to persistent backend data before presenting it as fully operational.

## Current Scope and Limitations

- Environmental values are only as reliable as their connected sensor, API, or sample data sources.
- Pollution forecasting should not be presented as scientifically validated unless the model, training data, evaluation metrics, and validation procedure are documented.
- Map-based regional access requires backend authorization and region-level data filtering, not only frontend display logic.
- Emergency reporting and committee coordination do not replace official emergency services.
- Before production use, authentication, authorization, input validation, audit logging, privacy, and security need to be reviewed.

## Future Improvements

- Integrate verified sensor feeds and document sensor units, sampling frequency, and data freshness.
- Add a documented forecasting pipeline with baseline comparisons and evaluation metrics.
- Enforce role-based and region-based access on the server.
- Add report status tracking, assignment, and resolution history.
- Add alerts for threshold breaches with configurable, documented thresholds.
- Improve accessibility, mobile responsiveness, testing, and deployment monitoring.

## Contributing

Contributions and suggestions are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make focused changes and test them.
4. Open a pull request with a description of the change and relevant screenshots or test results.

## License

Check the repository's license file before reusing or distributing this project. If no license is present, the code should not be assumed to be open source for unrestricted reuse.

---

Built as an environmental monitoring and community-response project.
