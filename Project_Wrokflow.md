flowchart TD
    subgraph Configuration
        A[config.yaml] --> B[Main Configuration]
        C[secrets.yaml] --> D[Sensitive Data]
        E[params.yaml] --> F[Model Parameters]
    end

    subgraph Core Components
        G[entity/] --> H[Data Models]
        I[src/config/] --> J[Config Management]
        K[components/] --> L[Project Components]
        M[pipeline/] --> N[Training Pipelines]
    end

    subgraph Development Flow
        O[Clone Repository] --> P[Install Dependencies]
        P --> Q[Initialize DVC]
        Q --> R[Run Pipeline]
    end

    subgraph Monitoring & Training
        S[TensorBoard] --> T[Model Monitoring]
        U[DVC] --> V[Pipeline Management]
        V --> W[Track Experiments]
    end

    subgraph Deployment
        X[Local Development] --> Y[Flask App]
        Z[Docker Deployment] --> AA[Build Image]
        AA --> AB[Run Container]
        AB --> AC[Push to Docker Hub]
    end

    R --> S
    R --> U
    Y --> AC
