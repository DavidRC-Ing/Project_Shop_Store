<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project Shop Store - A/B Testing Analysis</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background: white;
            margin-top: 20px;
            margin-bottom: 20px;
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }
        
        .header {
            text-align: center;
            padding: 40px 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 15px;
            margin-bottom: 30px;
        }
        
        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .header p {
            font-size: 1.2em;
            opacity: 0.9;
        }
        
        .badges {
            text-align: center;
            margin: 20px 0;
        }
        
        .badge {
            display: inline-block;
            padding: 8px 16px;
            margin: 5px;
            background: #667eea;
            color: white;
            border-radius: 20px;
            font-size: 0.9em;
            text-decoration: none;
        }
        
        .section {
            margin: 30px 0;
            padding: 20px;
            border-left: 4px solid #667eea;
            background: #f8f9fa;
            border-radius: 8px;
        }
        
        .section h2 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.8em;
        }
        
        .section h3 {
            color: #555;
            margin: 20px 0 10px 0;
            font-size: 1.3em;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .feature-card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            border-top: 4px solid #667eea;
        }
        
        .feature-card h4 {
            color: #667eea;
            margin-bottom: 10px;
        }
        
        .results-container {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
            margin: 20px 0;
        }
        
        .results-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .result-item {
            background: rgba(255,255,255,0.2);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
        }
        
        .result-number {
            font-size: 2em;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 20px 0;
        }
        
        .tech-item {
            background: #667eea;
            color: white;
            padding: 8px 15px;
            border-radius: 25px;
            font-size: 0.9em;
        }
        
        .image-placeholder {
            width: 100%;
            height: 300px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2em;
            margin: 20px 0;
        }
        
        .conclusions {
            background: #e8f5e8;
            border-left: 4px solid #28a745;
            padding: 20px;
            border-radius: 8px;
            margin: 20px 0;
        }
        
        .conclusions h3 {
            color: #28a745;
        }
        
        .footer {
            text-align: center;
            padding: 30px;
            background: #333;
            color: white;
            border-radius: 15px;
            margin-top: 30px;
        }
        
        .contact-links {
            margin-top: 20px;
        }
        
        .contact-links a {
            color: #667eea;
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.1em;
        }
        
        .contact-links a:hover {
            text-decoration: underline;
        }
        
        @media (max-width: 768px) {
            .container {
                margin: 10px;
                padding: 15px;
            }
            
            .header h1 {
                font-size: 2em;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>🛍️ Project Shop Store</h1>
            <p>Análisis Avanzado de Pruebas A/B para E-commerce</p>
        </div>
        
        <!-- Badges -->
        <div class="badges">
            <span class="badge">📊 Data Analysis</span>
            <span class="badge">🧪 A/B Testing</span>
            <span class="badge">📈 Statistical Analysis</span>
            <span class="badge">🛒 E-commerce</span>
            <span class="badge">🇪🇺 EU Market</span>
        </div>
        
        <!-- Descripción del Proyecto -->
        <div class="section">
            <h2>📋 Descripción del Proyecto</h2>
            <p>
                <strong>Project Shop Store</strong> es un análisis exhaustivo de pruebas A/B realizado para una tienda en línea internacional, 
                enfocado en evaluar el impacto de un sistema de recomendaciones mejorado y un embudo de pago optimizado sobre las 
                tasas de conversión de usuarios en la Unión Europea.
            </p>
            
            <div class="image-placeholder">
                📊 Dashboard de Análisis A/B Testing
                <br><small>Visualización de métricas de conversión</small>
            </div>
        </div>
        
        <!-- Características Principales -->
        <div class="section">
            <h2>✨ Características Principales</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <h4>🔍 Exploración de Datos</h4>
                    <p>Análisis profundo de la calidad y distribución de eventos de usuario, identificando patrones y anomalías en el comportamiento.</p>
                </div>
                
                <div class="feature-card">
                    <h4>🧹 Limpieza de Datos</h4>
                    <p>Procesamiento y limpieza automatizada de datasets, eliminando inconsistencias y preparando datos para análisis estadístico.</p>
                </div>
                
                <div class="feature-card">
                    <h4>📊 Análisis Estadístico</h4>
                    <p>Implementación de pruebas estadísticas automatizadas para comparar grupos de control y experimental con rigor científico.</p>
                </div>
                
                <div class="feature-card">
                    <h4>🎯 Sistema de Recomendaciones</h4>
                    <p>Evaluación del impacto de algoritmos de recomendación mejorados en la experiencia del usuario y conversiones.</p>
                </div>
                
                <div class="feature-card">
                    <h4>💳 Optimización de Checkout</h4>
                    <p>Análisis del embudo de pago optimizado y su efecto en la reducción de abandono de carrito.</p>
                </div>
                
                <div class="feature-card">
                    <h4>🌍 Enfoque Regional</h4>
                    <p>Análisis específico para el mercado de la Unión Europea, considerando regulaciones y comportamientos locales.</p>
                </div>
            </div>
        </div>
        
        <!-- Stack Tecnológico -->
        <div class="section">
            <h2>🛠️ Stack Tecnológico</h2>
            <div class="tech-stack">
                <span class="tech-item">Python</span>
                <span class="tech-item">Pandas</span>
                <span class="tech-item">NumPy</span>
                <span class="tech-item">SciPy</span>
                <span class="tech-item">Matplotlib</span>
                <span class="tech-item">Seaborn</span>
                <span class="tech-item">Jupyter Notebook</span>
                <span class="tech-item">Statistical Testing</span>
            </div>
        </div>
        
        <!-- Metodología -->
        <div class="section">
            <h2>🔬 Metodología</h2>
            <h3>1. Preparación de Datos</h3>
            <ul>
                <li>Extracción y validación de datos de eventos de usuario</li>
                <li>Limpieza y normalización de datasets</li>
                <li>Identificación y tratamiento de valores atípicos</li>
            </ul>
            
            <h3>2. Diseño Experimental</h3>
            <ul>
                <li>Definición de grupos de control y experimental</li>
                <li>Establecimiento de métricas clave (KPIs)</li>
                <li>Configuración de pruebas estadísticas</li>
            </ul>
            
            <h3>3. Análisis Estadístico</h3>
            <ul>
                <li>Pruebas de significancia estadística</li>
                <li>Análisis de distribuciones y varianzas</li>
                <li>Cálculo de intervalos de confianza</li>
            </ul>
            
            <div class="image-placeholder">
                📈 Gráficos de Distribución y Comparación
                <br><small>Visualización de resultados estadísticos</small>
            </div>
        </div>
        
        <!-- Resultados -->
        <div class="results-container">
            <h2>📊 Resultados Principales</h2>
            <div class="results-grid">
                <div class="result-item">
                    <div class="result-number">↗️</div>
                    <h4>Aumento de Actividad</h4>
                    <p>Incremento general en la actividad de usuarios</p>
                </div>
                
                <div class="result-item">
                    <div class="result-number">📊</div>
                    <h4>Sin Diferencias Significativas</h4>
                    <p>No se encontraron diferencias estadísticamente significativas en conversión</p>
                </div>
                
                <div class="result-item">
                    <div class="result-number">🎯</div>
                    <h4>Insights Valiosos</h4>
                    <p>Identificación de áreas de mejora para futuras pruebas</p>
                </div>
                
                <div class="result-item">
                    <div class="result-number">📋</div>
                    <h4>Recomendaciones</h4>
                    <p>Guías para optimización de experimentos futuros</p>
                </div>
            </div>
        </div>
        
        <!-- Conclusiones -->
        <div class="conclusions">
            <h3>🎯 Conclusiones Principales</h3>
            <ul>
                <li><strong>Diseño Experimental:</strong> La importancia de un diseño robusto fue confirmada a través del análisis riguroso de los datos.</li>
                <li><strong>Tamaño de Muestra:</strong> Se recomienda aumentar el tamaño de la muestra para detectar efectos más sutiles en futuras pruebas.</li>
                <li><strong>Variables Externas:</strong> Es crucial considerar factores externos que puedan influir en los resultados del experimento.</li>
                <li><strong>Métricas Adicionales:</strong> Explorar métricas complementarias puede proporcionar insights más profundos sobre el comportamiento del usuario.</li>
                <li><strong>Base Sólida:</strong> Los hallazgos proporcionan una fundación robusta para la toma de decisiones sobre implementación de nuevas funcionalidades.</li>
            </ul>
        </div>
        
        <!-- Instalación y Uso -->
        <div class="section">
            <h2>🚀 Instalación y Uso</h2>
            <h3>Prerrequisitos</h3>
            <pre style="background: #f4f4f4; padding: 15px; border-radius: 5px; overflow-x: auto;">
pip install pandas numpy scipy matplotlib seaborn jupyter
            </pre>
            
            <h3>Ejecución</h3>
            <pre style="background: #f4f4f4; padding: 15px; border-radius: 5px; overflow-x: auto;">
git clone https://github.com/tu-usuario/Project_Shop_Store.git
cd Project_Shop_Store
jupyter notebook
            </pre>
        </div>
        
        <!-- Estructura del Proyecto -->
        <div class="section">
            <h2>📁 Estructura del Proyecto</h2>
            <pre style="background: #f4f4f4; padding: 15px; border-radius: 5px; overflow-x: auto;">
Project_Shop_Store/
├── data/
│   ├── raw/                 # Datos originales
│   └── processed/           # Datos procesados
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_cleaning.ipynb
│   └── 03_ab_testing_analysis.ipynb
├── src/
│   ├── data_processing.py
│   ├── statistical_tests.py
│   └── visualization.py
├── results/
│   ├── figures/
│   └── reports/
└── README.md
            </pre>
        </div>
        
        <!-- Footer -->
        <div class="footer">
            <h3>👨‍💻 Desarrollado por [Tu Nombre]</h3>
            <p>Especialista en Data Science y Análisis Estadístico</p>
            <div class="contact-links">
                <a href="https://github.com/tu-usuario">GitHub</a>
                <a href="https://linkedin.com/in/tu-perfil">LinkedIn</a>
                <a href="mailto:tu-email@ejemplo.com">Email</a>
            </div>
        </div>
    </div>
</body>
</html>
