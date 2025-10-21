# registro_simposiumUTT
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registro - 3er Simposio del Día Mundial de la Alimentación 2025</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2c5aa0;
            --secondary: #3a7bd5;
            --accent: #ff7e5f;
            --light: #f8f9fa;
            --dark: #343a40;
            --success: #28a745;
            --danger: #dc3545;
            --warning: #ffc107;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4edf5 100%);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
        }
        
        .header {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            padding: 2.5rem 2rem;
            border-radius: 15px;
            margin-bottom: 2rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.1)"/></svg>');
            background-size: cover;
        }
        
        .header-content {
            position: relative;
            z-index: 1;
        }
        
        .card {
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            margin-bottom: 1.5rem;
            border: none;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .card-header {
            background: linear-gradient(135deg, var(--secondary) 0%, var(--primary) 100%);
            color: white;
            border-radius: 12px 12px 0 0 !important;
            padding: 1.2rem 1.5rem;
            font-weight: 600;
        }
        
        .btn-primary {
            background: linear-gradient(135deg, var(--secondary) 0%, var(--primary) 100%);
            border: none;
            padding: 0.7rem 1.5rem;
            font-weight: 600;
            border-radius: 8px;
            transition: all 0.3s ease;
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(58, 123, 213, 0.4);
        }
        
        .taller-card {
            transition: all 0.3s ease;
            cursor: pointer;
            height: 100%;
        }
        
        .taller-card:hover {
            transform: translateY(-5px);
        }
        
        .taller-selected {
            border: 2px solid var(--secondary);
            background-color: #f0f7ff;
        }
        
        .taller-full {
            background-color: #fff5f5;
            border: 1px solid #f5c6cb;
            opacity: 0.8;
        }
        
        .badge-full {
            background-color: var(--danger);
        }
        
        .horario-section {
            margin-bottom: 2rem;
            padding: 1.5rem;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
        }
        
        .horario-title {
            color: var(--primary);
            border-bottom: 2px solid var(--secondary);
            padding-bottom: 0.5rem;
            margin-bottom: 1.5rem;
            font-weight: 700;
        }
        
        .progress {
            height: 10px;
            border-radius: 5px;
        }
        
        /* Estilos para la constancia tipo PowerPoint */
        .constancia-powerpoint {
            background: linear-gradient(135deg, #1a3a6a 0%, #2c5aa0 100%);
            color: white;
            min-height: 600px;
            border-radius: 15px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 3rem;
        }
        
        .constancia-powerpoint::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: 
                radial-gradient(circle at 20% 80%, rgba(255,255,255,0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(255,255,255,0.05) 0%, transparent 50%);
            pointer-events: none;
        }
        
        .constancia-logo {
            text-align: center;
            margin-bottom: 2rem;
        }
        
        .logo-circle {
            width: 120px;
            height: 120px;
            background: white;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }
        
        .logo-text {
            color: #2c5aa0;
            font-weight: 800;
            font-size: 1.8rem;
            line-height: 1;
        }
        
        .constancia-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .constancia-main-title {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 1rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .constancia-subtitle {
            font-size: 1.8rem;
            font-weight: 300;
            margin-bottom: 0.5rem;
        }
        
        .constancia-institution {
            font-size: 1.4rem;
            font-weight: 600;
            color: #a8d1ff;
        }
        
        .constancia-body {
            text-align: center;
            margin: 2rem 0;
        }
        
        .constancia-to {
            font-size: 1.8rem;
            margin-bottom: 2rem;
            font-weight: 300;
        }
        
        .constancia-name {
            font-size: 2.5rem;
            font-weight: 700;
            margin: 2rem 0;
            padding: 1.5rem;
            background: rgba(255,255,255,0.1);
            border-radius: 10px;
            border: 2px solid rgba(255,255,255,0.2);
            backdrop-filter: blur(10px);
        }
        
        .constancia-text {
            font-size: 1.3rem;
            line-height: 1.6;
            margin-bottom: 1.5rem;
            font-weight: 300;
        }
        
        .constancia-event {
            font-weight: 600;
            color: #a8d1ff;
        }
        
        .constancia-footer {
            margin-top: 3rem;
            text-align: center;
            border-top: 1px solid rgba(255,255,255,0.2);
            padding-top: 2rem;
        }
        
        .constancia-date {
            font-size: 1.2rem;
            font-weight: 300;
        }
        
        .constancia-place {
            font-size: 1.1rem;
            font-weight: 300;
            color: #a8d1ff;
            margin-top: 0.5rem;
        }
        
        footer {
            text-align: center;
            margin-top: 3rem;
            padding: 2rem;
            color: #6c757d;
            font-size: 0.9rem;
            border-top: 1px solid #e9ecef;
        }
        
        .form-label {
            font-weight: 600;
            color: var(--dark);
            margin-bottom: 0.5rem;
        }
        
        .form-control, .form-select {
            border-radius: 8px;
            padding: 0.7rem 1rem;
            border: 1px solid #ced4da;
            transition: all 0.3s ease;
        }
        
        .form-control:focus, .form-select:focus {
            border-color: var(--secondary);
            box-shadow: 0 0 0 0.25rem rgba(58, 123, 213, 0.25);
        }
        
        .step-indicator {
            display: flex;
            justify-content: space-between;
            margin-bottom: 2rem;
            position: relative;
        }
        
        .step-indicator::before {
            content: '';
            position: absolute;
            top: 15px;
            left: 0;
            right: 0;
            height: 2px;
            background-color: #e9ecef;
            z-index: 1;
        }
        
        .step {
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            z-index: 2;
        }
        
        .step-number {
            width: 35px;
            height: 35px;
            border-radius: 50%;
            background-color: #e9ecef;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: #6c757d;
        }
        
        .step.active .step-number {
            background-color: var(--primary);
            color: white;
        }
        
        .step.completed .step-number {
            background-color: var(--success);
            color: white;
        }
        
        .step-label {
            font-size: 0.85rem;
            font-weight: 600;
            color: #6c757d;
        }
        
        .step.active .step-label {
            color: var(--primary);
        }
        
        .admin-panel {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 10px;
            padding: 1.5rem;
        }
        
        .taller-info {
            font-size: 0.85rem;
            color: #6c757d;
        }
        
        .seleccionados-container {
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .seleccionados-list {
            list-style-type: none;
            padding: 0;
        }
        
        .seleccionados-list li {
            padding: 0.5rem 0;
            border-bottom: 1px solid #e9ecef;
        }
        
        .seleccionados-list li:last-child {
            border-bottom: none;
        }
        
        .alert-custom {
            border-radius: 10px;
            padding: 1rem 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .taller-counter {
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            width: 25px;
            height: 25px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            margin-right: 0.5rem;
        }
        
        .stats-card {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 10px;
            padding: 1.5rem;
            margin-bottom: 1rem;
        }
        
        .stats-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .stats-label {
            font-size: 0.9rem;
            color: #6c757d;
            font-weight: 600;
        }
        
        @media (max-width: 768px) {
            .header {
                padding: 1.5rem 1rem;
            }
            
            .constancia-powerpoint {
                padding: 2rem 1.5rem;
                min-height: 500px;
            }
            
            .constancia-main-title {
                font-size: 2.5rem;
            }
            
            .constancia-subtitle {
                font-size: 1.4rem;
            }
            
            .constancia-name {
                font-size: 2rem;
                padding: 1rem;
            }
            
            .constancia-text {
                font-size: 1.1rem;
            }
            
            .step-label {
                font-size: 0.75rem;
            }
        }
        
        @media print {
            .card:not(.constancia-container), .header, footer, .step-indicator, .btn, .progress {
                display: none !important;
            }
            
            .constancia-container {
                box-shadow: none !important;
                border: none !important;
                margin: 0 !important;
                padding: 0 !important;
            }
            
            .constancia-powerpoint {
                box-shadow: none !important;
                page-break-inside: avoid;
                min-height: 100vh;
                border-radius: 0;
            }
            
            body {
                background: white !important;
            }
        }
    </style>
</head>
<body>
    <div class="container my-5">
        <!-- Encabezado -->
        <div class="header text-center">
            <div class="header-content">
                <h1 class="display-5 fw-bold">3er Simposio del Día Mundial de la Alimentación</h1>
                <p class="lead fs-4">Universidad Tecnológica de Tehuacán</p>
                <p class="mb-0 fs-5">23 y 24 de Octubre de 2025</p>
                <p class="mt-2 fs-6">"Mano a mano por unos alimentos y un futuro mejores"</p>
            </div>
        </div>

        <!-- Indicador de pasos -->
        <div class="step-indicator">
            <div class="step active">
                <div class="step-number">1</div>
                <div class="step-label">Registro</div>
            </div>
            <div class="step">
                <div class="step-number">2</div>
                <div class="step-label">Talleres</div>
            </div>
            <div class="step">
                <div class="step-number">3</div>
                <div class="step-label">Confirmación</div>
            </div>
        </div>

        <!-- Formulario de registro -->
        <div class="card">
            <div class="card-header">
                <h2 class="mb-0"><i class="fas fa-user-plus me-2"></i>Registro de Estudiantes</h2>
            </div>
            <div class="card-body">
                <form id="registroForm">
                    <div class="row mb-4">
                        <div class="col-md-6 mb-3">
                            <label for="nombre" class="form-label">Nombre completo</label>
                            <input type="text" class="form-control" id="nombre" required>
                            <div class="invalid-feedback">Por favor ingresa tu nombre completo</div>
                        </div>
                        <div class="col-md-6 mb-3">
                            <label for="matricula" class="form-label">Matrícula</label>
                            <input type="text" class="form-control" id="matricula" required>
                            <div class="invalid-feedback">Por favor ingresa tu matrícula</div>
                        </div>
                    </div>
                    <div class="row mb-4">
                        <div class="col-md-6 mb-3">
                            <label for="email" class="form-label">Correo electrónico</label>
                            <input type="email" class="form-control" id="email" required>
                            <div class="invalid-feedback">Por favor ingresa un correo válido</div>
                        </div>
                        <div class="col-md-6 mb-3">
                            <label for="cuatrimestre" class="form-label">Cuatrimestre</label>
                            <select class="form-select" id="cuatrimestre" required>
                                <option value="">Selecciona tu cuatrimestre</option>
                                <option value="1°">1° Cuatrimestre</option>
                                <option value="4°">4° Cuatrimestre</option>
                                <option value="7°">7° Cuatrimestre</option>
                                <option value="10°">10° Cuatrimestre</option>
                            </select>
                            <div class="invalid-feedback">Por favor selecciona tu cuatrimestre</div>
                        </div>
                    </div>
                    
                    <!-- Selección de talleres del día 23 -->
                    <div class="mb-4">
                        <h4 class="mb-3"><i class="fas fa-wrench me-2"></i>Selecciona 2 talleres para el día 23 de octubre</h4>
                        <p class="text-muted mb-4">Puedes seleccionar cualquier combinación de talleres, sin restricciones de horario.</p>
                        
                        <!-- Alert para mostrar estado de selección -->
                        <div id="alertSeleccion" class="alert alert-info alert-custom" style="display: none;">
                            <i class="fas fa-info-circle me-2"></i>
                            <span id="alertText"></span>
                        </div>
                        
                        <!-- Talleres seleccionados -->
                        <div class="seleccionados-container">
                            <h5 class="mb-3"><i class="fas fa-check-circle me-2 text-success"></i>Talleres Seleccionados</h5>
                            <ul class="seleccionados-list" id="talleresSeleccionadosList">
                                <li class="text-muted">Aún no has seleccionado talleres</li>
                            </ul>
                        </div>
                        
                        <!-- Mañana 8:00-11:00 -->
                        <div class="horario-section">
                            <h5 class="horario-title"><i class="far fa-sun me-2"></i>Horario de Mañana (8:00 - 11:00 h)</h5>
                            <div id="talleresMananaContainer" class="row">
                                <!-- Los talleres de mañana se cargarán aquí -->
                            </div>
                        </div>
                        
                        <!-- Tarde 12:00-15:00 -->
                        <div class="horario-section">
                            <h5 class="horario-title"><i class="far fa-moon me-2"></i>Horario de Tarde (12:00 - 15:00 h)</h5>
                            <div id="talleresTardeContainer" class="row">
                                <!-- Los talleres de tarde se cargarán aquí -->
                            </div>
                        </div>
                        
                        <div class="mt-2 text-muted">
                            <small><i class="fas fa-info-circle me-1"></i> Cada taller tiene un límite de 30 participantes</small>
                        </div>
                    </div>
                    
                    <div class="d-grid">
                        <button type="submit" class="btn btn-primary btn-lg py-2">
                            <i class="fas fa-paper-plane me-2"></i>Completar Registro
                        </button>
                    </div>
                </form>
            </div>
        </div>

        <!-- Área de administración (solo para organizadores) -->
        <div class="card mt-4">
            <div class="card-header">
                <h2 class="mb-0"><i class="fas fa-tools me-2"></i>Panel de Administración</h2>
            </div>
            <div class="card-body">
                <div class="admin-panel">
                    <div class="mb-3">
                        <label for="adminPassword" class="form-label">Contraseña de administrador</label>
                        <input type="password" class="form-control" id="adminPassword" placeholder="Ingresa la contraseña">
                    </div>
                    <button id="adminBtn" class="btn btn-outline-primary">
                        <i class="fas fa-lock me-2"></i>Acceder
                    </button>
                    
                    <div id="adminPanel" class="mt-4" style="display: none;">
                        <!-- Estadísticas generales -->
                        <div class="row mb-4">
                            <div class="col-md-3">
                                <div class="stats-card text-center">
                                    <div class="stats-number" id="totalInscritos">0</div>
                                    <div class="stats-label">Total Inscritos</div>
                                </div>
                            </div>
                            <div class="col-md-3">
                                <div class="stats-card text-center">
                                    <div class="stats-number" id="talleresLlenos">0</div>
                                    <div class="stats-label">Talleres Llenos</div>
                                </div>
                            </div>
                            <div class="col-md-3">
                                <div class="stats-card text-center">
                                    <div class="stats-number" id="talleresDisponibles">0</div>
                                    <div class="stats-label">Talleres Disponibles</div>
                                </div>
                            </div>
                            <div class="col-md-3">
                                <div class="stats-card text-center">
                                    <div class="stats-number" id="porcentajeAsistencia">0%</div>
                                    <div class="stats-label">Asistencia Promedio</div>
                                </div>
                            </div>
                        </div>
                        
                        <h5><i class="fas fa-users me-2"></i>Lista de inscritos por taller</h5>
                        <div id="listaTalleresAdmin" class="mb-4">
                            <!-- Lista de talleres con inscritos -->
                        </div>
                        
                        <h5><i class="fas fa-clipboard-check me-2"></i>Control de asistencia</h5>
                        <div class="mb-3">
                            <label for="selectTallerAsistencia" class="form-label">Seleccionar taller</label>
                            <select class="form-select" id="selectTallerAsistencia">
                                <!-- Opciones de talleres -->
                            </select>
                        </div>
                        <div id="listaAsistencia" class="mb-4">
                            <!-- Lista de estudiantes para pasar lista -->
                        </div>
                        
                        <div class="mt-4">
                            <button id="exportarDatos" class="btn btn-success">
                                <i class="fas fa-file-export me-2"></i>Exportar Datos
                            </button>
                            <button id="limpiarDatos" class="btn btn-danger ms-2">
                                <i class="fas fa-trash me-2"></i>Limpiar Todos los Datos
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Área de constancias -->
        <div class="card mt-4 constancia-container">
            <div class="card-header">
                <h2 class="mb-0"><i class="fas fa-certificate me-2"></i>Reconocimiento de Participación</h2>
            </div>
            <div class="card-body p-0">
                <div class="constancia-powerpoint">
                    <!-- Logo UTT -->
                    <div class="constancia-logo">
                        <div class="logo-circle">
                            <div class="logo-text">UTT</div>
                        </div>
                    </div>
                    
                    <!-- Título principal -->
                    <div class="constancia-title">
                        <h1 class="constancia-main-title">Reconocimiento</h1>
                        <div class="constancia-subtitle">La Universidad Tecnológica de Tehuacán</div>
                        <div class="constancia-institution">Otorga el presente</div>
                    </div>
                    
                    <!-- Cuerpo del reconocimiento -->
                    <div class="constancia-body">
                        <div class="constancia-to">A:</div>
                        <div class="constancia-name" id="nombreConstancia">[Nombre del Estudiante]</div>
                        
                        <div class="constancia-text">
                            Por su destacada participación en el 3er Simposio
                        </div>
                        <div class="constancia-text">
                            <span class="constancia-event">"Día Mundial de la Alimentación 2025"</span>
                        </div>
                        <div class="constancia-text">
                            realizado los días 23 y 24 de octubre del presente año
                        </div>
                    </div>
                    
                    <!-- Pie de página -->
                    <div class="constancia-footer">
                        <div class="constancia-date">Tehuacán, Puebla, Octubre 2025</div>
                        <div class="constancia-place">Universidad Tecnológica de Tehuacán</div>
                    </div>
                </div>
                
                <!-- Progreso de asistencia y botón de impresión -->
                <div class="p-4">
                    <div class="progress mb-3">
                        <div id="progresoAsistencia" class="progress-bar" role="progressbar" style="width: 0%;" 
                             aria-valuenow="0" aria-valuemin="0" aria-valuemax="100">0%</div>
                    </div>
                    <small class="text-muted d-block mb-3">Progreso de asistencia (requerido 85-90% para reconocimiento)</small>
                    
                    <div class="text-center">
                        <button id="imprimirConstancia" class="btn btn-primary" disabled>
                            <i class="fas fa-print me-2"></i>Imprimir Reconocimiento
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>Universidad Tecnológica de Tehuacán | Programa de Conferencias y Talleres Alimentos</p>
        <p>23 y 24 de Octubre | "Mano a mano por unos alimentos y un futuro mejores"</p>
    </footer>

    <script>
        // Datos de los talleres del 23 de octubre organizados por horarios
        const talleres = {
            manana: [
                { 
                    id: 'taller1-manana', 
                    nombre: 'Alimentación adecuada y sostenible para la salud y rendimiento físico', 
                    horario: '08:00 - 11:00 h', 
                    lugar: 'Sala Audiovisual del Edificio A',
                    instructores: 'MNA. Alejo Enrique Guerrero Alarcón',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller2', 
                    nombre: 'Elaboración de cremas Cosméticas', 
                    horario: '08:00 - 11:00 h', 
                    lugar: 'Lab. De Fisiocquímica',
                    instructores: 'Dr. Humberto Rafael Bravo',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller3', 
                    nombre: 'Fundamentos de la Extracción Fitoquímica', 
                    horario: '08:00 - 11:00 h', 
                    lugar: 'Lab. de Microbiología',
                    instructores: 'Ingeniero Farmacobiólogo Eulalio Miguel Valiente Flores',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller5', 
                    nombre: 'Producción de hongo seta (Pleurotus ostreatus)', 
                    horario: '08:00 - 11:00 h', 
                    lugar: 'Laboratorio de Microbiología',
                    instructores: 'Mtra. Patricia Hernández Herrera',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller6', 
                    nombre: '¡No más Word! Escribe tu Tesis en, LaTeX, un Editor de Textos Científicos', 
                    horario: '08:00 - 11:00 h', 
                    lugar: 'LC-Alimentos',
                    instructores: 'Dr. Jacinto Sandoval Lira',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller7', 
                    nombre: 'Determinación de vida de anaquel acelerada', 
                    horario: '08:00 - 11:00 h', 
                    lugar: 'Lab de computo de ACSYP y Lab de Inv y transferencia',
                    instructores: 'Mtro Miguel García Flores / Cecilia García Santos',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller8', 
                    nombre: 'Cálculo dietosintético y distribución de macronutrientes', 
                    horario: '08:00 - 11:00 h', 
                    lugar: 'Sala de Biblioteca',
                    instructores: 'Ing. Areli Ramírez Moreno',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller9-manana', 
                    nombre: 'Taller de Elaboración de Helado', 
                    horario: '08:00 - 12:00 h', 
                    lugar: 'Taller de Lácteos',
                    instructores: 'Mtro. Carlos Roberto Camarillo Rojas',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller4-manana', 
                    nombre: 'Diseño de etiquetas para productos alimenticios', 
                    horario: '09:00 - 11:00 h', 
                    lugar: 'Lab de computo de TICs',
                    instructores: 'Mtra Alejandra Velasco Reyes',
                    cupo: 30,
                    inscritos: []
                }
            ],
            tarde: [
                { 
                    id: 'taller1-tarde', 
                    nombre: 'Etiquetado nutricional', 
                    horario: '12:00 - 15:00 h', 
                    lugar: 'Sala Audiovisual del Edificio A',
                    instructores: 'L.N Ángel Aparicio Alfaro',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller2-tarde', 
                    nombre: 'Elaboración de cremas Cosméticas', 
                    horario: '12:00 - 15:00 h', 
                    lugar: 'Lab. De Fisiocquímica',
                    instructores: 'Dr. Humberto Rafael Bravo',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller3-tarde', 
                    nombre: 'Fundamentos de la Extracción Fitoquímica', 
                    horario: '12:00 - 15:00 h', 
                    lugar: 'Lab. de Microbiología',
                    instructores: 'Ingeniero Farmacobiólogo Eulalio Miguel Valiente Flores',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller5-tarde', 
                    nombre: 'Producción de hongo seta (Pleurotus ostreatus)', 
                    horario: '12:00 - 15:00 h', 
                    lugar: 'Laboratorio de Microbiología',
                    instructores: 'Mtra. Patricia Hernández Herrera',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller6-tarde', 
                    nombre: '¡No más Word! Escribe tu Tesis en, LaTeX, un Editor de Textos Científicos', 
                    horario: '12:00 - 15:00 h', 
                    lugar: 'LC-Alimentos',
                    instructores: 'Dr. Jacinto Sandoval Lira',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller7-tarde', 
                    nombre: 'Determinación de vida de anaquel acelerada', 
                    horario: '12:00 - 15:00 h', 
                    lugar: 'Lab de computo de ACSYP y Lab de Inv y transferencia',
                    instructores: 'Mtro Miguel García Flores / Cecilia García Santos',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller8-tarde', 
                    nombre: 'Cálculo dietosintético y distribución de macronutrientes', 
                    horario: '12:00 - 15:00 h', 
                    lugar: 'Sala de Biblioteca',
                    instructores: 'Ing. Areli Ramírez Moreno',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller9-tarde', 
                    nombre: 'Taller de Elaboración de Helado', 
                    horario: '12:00 - 16:00 h', 
                    lugar: 'Taller de Lácteos',
                    instructores: 'Mtro. Carlos Roberto Camarillo Rojas',
                    cupo: 30,
                    inscritos: []
                },
                { 
                    id: 'taller4-tarde', 
                    nombre: 'Diseño de etiquetas para productos alimenticios', 
                    horario: '13:00 - 15:00 h', 
                    lugar: 'Lab de computo de TICs',
                    instructores: 'Mtra Alejandra Velasco Reyes',
                    cupo: 30,
                    inscritos: []
                }
            ]
        };

        // Variables globales
        let estudiantesRegistrados = [];
        let talleresSeleccionados = [];
        
        // Inicializar la aplicación
        document.addEventListener('DOMContentLoaded', function() {
            cargarDatosGuardados();
            cargarTalleres();
            inicializarEventos();
        });
        
        // Cargar datos guardados del localStorage
        function cargarDatosGuardados() {
            // Cargar estudiantes registrados
            const estudiantesGuardados = localStorage.getItem('estudiantesRegistrados');
            if (estudiantesGuardados) {
                estudiantesRegistrados = JSON.parse(estudiantesGuardados);
            }
            
            // Cargar datos de talleres
            const talleresGuardados = localStorage.getItem('talleresData');
            if (talleresGuardados) {
                const talleresData = JSON.parse(talleresGuardados);
                
                // Actualizar los arrays de inscritos en cada taller
                for (const grupo in talleres) {
                    talleres[grupo].forEach(taller => {
                        const tallerGuardado = talleresData[grupo].find(t => t.id === taller.id);
                        if (tallerGuardado) {
                            taller
