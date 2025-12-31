graph TD
    %% Inicio del Proceso
    A((Idea Política)) -->|Entrada Libre| B(IntakeHN_GCHI)
    
    %% Fase de Estructuración
    B -->|Genera Pasaporte + ID| C{¿Qué Eje es?}
    
    %% Fase de Diseño (Ejes Especializados)
    C -->|Agro| D1(AgroHN_GCHI)
    C -->|Infraestructura| D2(InfraHN_GCHI)
    C -->|Gobierno Digital| D3(EstadoDigitalHN_GCHI)
    C -->|Otros Ejes| D4(EjeEspecifico_GCHI)
    
    %% Fase de Coordinación e Integridad
    D1 & D2 & D3 & D4 -->|Diseño Técnico| E(GobernanzaHN_GCHI)
    E -->|Mapa de Actores| F(LegalCheckerHN_GCHI)
    
    %% El Filtro Crítico
    F -->|NO APTO| G[Regresa a Diseño para Ajustes]
    G --> D1 & D2 & D3 & D4
    
    F -->|APTO / CON AJUSTES| H(PresupuestoHN_GCHI)
    
    %% Fase de Validación de Realidad
    H -->|Viabilidad Fiscal| I(RiesgosHN_GCHI)
    I -->|Plan de Mitigación| J(LegisDraftHN_GCHI)
    
    %% Salida Institucional
    J -->|Borrador Normativo| K(LegalCheckerHN_GCHI - Final)
    K -->|VALIDACIÓN TOTAL| L((SALIDA INSTITUCIONAL))
    
    %% Estilo de los nodos
    style B fill:#e1f5fe,stroke:#01579b
    style F fill:#ffebee,stroke:#b71c1c
    style L fill:#e8f5e9,stroke:#1b5e20
    style J fill:#fff3e0,stroke:#e65100
