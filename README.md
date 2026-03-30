# COSASVARIAS
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Falacias Lógicas — Infografía</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=IBM+Plex+Mono:wght@400;600&family=IBM+Plex+Sans:wght@300;400;600&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d0f14;
    --surface: #13161e;
    --border: #1e2330;
    --accent1: #e8c547;
    --accent2: #e05c5c;
    --accent3: #5cc8e0;
    --accent4: #a07ee8;
    --accent5: #5ce08a;
    --accent6: #e08a5c;
    --accent7: #e05ca0;
    --text: #e8eaf0;
    --muted: #7a8099;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'IBM Plex Sans', sans-serif;
    min-height: 100vh;
    padding: 40px 20px 60px;
  }

  /* HEADER */
  header {
    text-align: center;
    margin-bottom: 60px;
    position: relative;
  }
  header::before {
    content: '';
    display: block;
    width: 2px;
    height: 40px;
    background: var(--accent1);
    margin: 0 auto 20px;
  }
  .header-label {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    letter-spacing: 4px;
    color: var(--accent1);
    text-transform: uppercase;
    margin-bottom: 12px;
  }
  h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(36px, 6vw, 72px);
    font-weight: 900;
    line-height: 1;
    color: var(--text);
    margin-bottom: 16px;
  }
  h1 span {
    color: var(--accent1);
  }
  .header-sub {
    font-size: 14px;
    color: var(--muted);
    max-width: 500px;
    margin: 0 auto;
    line-height: 1.6;
  }

  /* LAYOUT */
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }

  /* CATEGORY */
  .category {
    margin-bottom: 50px;
  }
  .category-header {
    display: flex;
    align-items: center;
    gap: 14px;
    margin-bottom: 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
  }
  .category-dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    flex-shrink: 0;
  }
  .category-title {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
  }
  .category-count {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    margin-left: auto;
  }

  /* GRID */
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 14px;
  }

  /* CARD */
  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 20px;
    position: relative;
    overflow: hidden;
    transition: transform 0.2s, border-color 0.2s;
  }
  .card:hover {
    transform: translateY(-2px);
  }
  .card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 3px;
    height: 100%;
  }
  .card-name {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 12px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 8px;
  }
  .card-latin {
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    margin-bottom: 10px;
    font-style: italic;
  }
  .card-desc {
    font-size: 13px;
    line-height: 1.6;
    color: #b0b8cc;
  }
  .card-tag {
    display: inline-block;
    margin-top: 10px;
    font-family: 'IBM Plex Mono', monospace;
    font-size: 10px;
    padding: 3px 8px;
    border-radius: 3px;
    opacity: 0.7;
  }

  /* Color themes per category */
  .cat-1 { --c: var(--accent1); }
  .cat-2 { --c: var(--accent2); }
  .cat-3 { --c: var(--accent3); }
  .cat-4 { --c: var(--accent4); }
  .cat-5 { --c: var(--accent5); }
  .cat-6 { --c: var(--accent6); }
  .cat-7 { --c: var(--accent7); }
  .cat-8 { --c: #e8c547; }
  .cat-9 { --c: #5cc8e0; }
  .cat-10 { --c: #e05c5c; }
  .cat-11 { --c: #a07ee8; }
  .cat-12 { --c: #5ce08a; }

  .category-dot { background: var(--c); }
  .category-title { color: var(--c); }
  .card::before { background: var(--c); }
  .card:hover { border-color: var(--c); }
  .card-name { color: var(--c); }
  .card-tag { background: color-mix(in srgb, var(--c) 15%, transparent); color: var(--c); }

  /* FOOTER */
  footer {
    text-align: center;
    margin-top: 60px;
    padding-top: 30px;
    border-top: 1px solid var(--border);
    font-family: 'IBM Plex Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 2px;
  }
  footer span { color: var(--accent1); }
</style>
</head>
<body>

<div class="container">

  <header>
    <div class="header-label">Guía de referencia completa</div>
    <h1>Falacias <span>Lógicas</span></h1>
    <p class="header-sub">Catálogo de errores argumentativos: definición y clave de identificación para cada tipo de razonamiento inválido.</p>
  </header>

  <!-- 1. DISTRACCIONES -->
  <div class="category cat-1">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Falacias de Distracción</div>
      <div class="category-count">04 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Falso Dilema</div>
        <div class="card-desc">Se presentan solo dos opciones como si fueran las únicas posibles, ignorando alternativas válidas. Uso ilegítimo del operador "o".</div>
        <span class="card-tag">→ Busca la opción omitida</span>
      </div>
      <div class="card">
        <div class="card-name">Argumento de la Ignorancia</div>
        <div class="card-latin">argumentum ad ignorantiam</div>
        <div class="card-desc">Se asume que algo es verdadero porque no se ha demostrado falso, o falso porque no se ha demostrado verdadero.</div>
        <span class="card-tag">→ Ausencia de prueba ≠ prueba de ausencia</span>
      </div>
      <div class="card">
        <div class="card-name">Pendiente Resbaladiza</div>
        <div class="card-desc">Se afirma que aceptar una proposición desencadenará inevitablemente una serie de consecuencias negativas, sin justificar ese vínculo causal. Uso ilegítimo de "si… entonces".</div>
        <span class="card-tag">→ Demuestra que el efecto final no es inevitable</span>
      </div>
      <div class="card">
        <div class="card-name">Pregunta Compleja</div>
        <div class="card-desc">Dos proposiciones separadas se fusionan en una sola, obligando a aceptar o rechazar ambas a la vez. Uso ilegítimo del operador "y".</div>
        <span class="card-tag">→ Separa las proposiciones ocultas</span>
      </div>
    </div>
  </div>

  <!-- 2. APELACIONES A MOTIVOS -->
  <div class="category cat-2">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Apelación a los Motivos en lugar de Apoyo</div>
      <div class="category-count">05 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Recurso a la Fuerza</div>
        <div class="card-latin">argumentum ad baculum</div>
        <div class="card-desc">Se usa una amenaza implícita o explícita para forzar la aceptación de una conclusión. La intimidación no reemplaza al argumento.</div>
        <span class="card-tag">→ La amenaza no afecta la verdad de la proposición</span>
      </div>
      <div class="card">
        <div class="card-name">Apelación a la Lástima</div>
        <div class="card-latin">argumentum ad misericordiam</div>
        <div class="card-desc">Se pide aceptar una conclusión apelando al estado deplorable o el esfuerzo del argumentador, en vez de ofrecer razones válidas.</div>
        <span class="card-tag">→ El lamento no prueba la conclusión</span>
      </div>
      <div class="card">
        <div class="card-name">Apelación a las Consecuencias</div>
        <div class="card-latin">argumentum ad consequentiam</div>
        <div class="card-desc">Se afirma que una creencia es falsa porque sus consecuencias serían desagradables. Lo que queremos que sea verdad no determina lo que es verdad.</div>
        <span class="card-tag">→ Las consecuencias no determinan la verdad</span>
      </div>
      <div class="card">
        <div class="card-name">Lenguaje Perjudicial</div>
        <div class="card-desc">Se usan términos emotivos o moralmente cargados para presionar a aceptar una posición, insinuando que quien disiente es moralmente inferior.</div>
        <span class="card-tag">→ Identifica el término emotivo sesgado</span>
      </div>
      <div class="card">
        <div class="card-name">Apelación a la Popularidad</div>
        <div class="card-latin">argumentum ad populum</div>
        <div class="card-desc">Se asume que una proposición es verdadera porque mucha gente la cree. La opinión mayoritaria no es garantía de verdad.</div>
        <span class="card-tag">→ La popularidad no es evidencia</span>
      </div>
    </div>
  </div>

  <!-- 3. CAMBIAR DE TEMA -->
  <div class="category cat-3">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Cambiar de Tema</div>
      <div class="category-count">04 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Atacando a la Persona</div>
        <div class="card-latin">argumentum ad hominem</div>
        <div class="card-desc">Se ataca a quien formula el argumento —su carácter, circunstancias o contradicciones— en lugar de refutar el argumento mismo. Formas: abusivo, circunstancial y tu quoque.</div>
        <span class="card-tag">→ El carácter no invalida el argumento</span>
      </div>
      <div class="card">
        <div class="card-name">Recurso a la Autoridad</div>
        <div class="card-latin">argumentum ad verecundiam</div>
        <div class="card-desc">Se cita a una autoridad como prueba en un campo donde no es experta, o donde los expertos no tienen consenso. Incluye el recurso al rumor.</div>
        <span class="card-tag">→ Verifica si la autoridad es competente y hay consenso</span>
      </div>
      <div class="card">
        <div class="card-name">Estilo sobre Sustancia</div>
        <div class="card-desc">La forma en que se presenta el argumento (o el presentador) se toma como indicador de que la conclusión es verdadera, ignorando el contenido real.</div>
        <span class="card-tag">→ El estilo no cambia la verdad de la conclusión</span>
      </div>
      <div class="card">
        <div class="card-name">Autoridad Anónima</div>
        <div class="card-desc">Se invoca una fuente de autoridad sin nombrarla, lo que hace imposible evaluar su credibilidad. Variante: la apelación al rumor.</div>
        <span class="card-tag">→ Sin fuente identificable, no hay credibilidad evaluable</span>
      </div>
    </div>
  </div>

  <!-- 4. INDUCTIVAS -->
  <div class="category cat-4">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Falacias Inductivas</div>
      <div class="category-count">05 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Generalización Apresurada</div>
        <div class="card-desc">Se extrae una conclusión general a partir de una muestra demasiado pequeña o insuficiente para representar a la población.</div>
        <span class="card-tag">→ Señala que la muestra es demasiado pequeña</span>
      </div>
      <div class="card">
        <div class="card-name">Muestra No Representativa</div>
        <div class="card-desc">La muestra utilizada difiere de la población de forma relevante, por lo que la conclusión no puede extrapolarse correctamente al conjunto.</div>
        <span class="card-tag">→ Muestra en qué es diferente la muestra</span>
      </div>
      <div class="card">
        <div class="card-name">Falsa Analogía</div>
        <div class="card-desc">Se comparan dos elementos A y B y se transfiere una propiedad de A a B, ignorando diferencias relevantes que invalidan la comparación.</div>
        <span class="card-tag">→ Identifica la diferencia que invalida la analogía</span>
      </div>
      <div class="card">
        <div class="card-name">Inducción Perezosa</div>
        <div class="card-desc">Se niega la conclusión correcta de una inferencia inductiva a pesar de contar con evidencia sólida que la respalda.</div>
        <span class="card-tag">→ Señala la fortaleza de la inferencia ignorada</span>
      </div>
      <div class="card">
        <div class="card-name">Falacia de Exclusión</div>
        <div class="card-desc">Se omite evidencia relevante que, de incluirse, cambiaría la conclusión del argumento. Viola el "principio de prueba total".</div>
        <span class="card-tag">→ Presenta la evidencia omitida y muestra cómo cambia la conclusión</span>
      </div>
    </div>
  </div>

  <!-- 5. SILOGISMOS ESTADÍSTICOS -->
  <div class="category cat-5">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Falacias con Silogismos Estadísticos</div>
      <div class="category-count">02 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Accidente</div>
        <div class="card-desc">Se aplica una regla general a un caso particular donde las circunstancias indican que debería hacerse una excepción.</div>
        <span class="card-tag">→ La regla general tiene excepciones aplicables aquí</span>
      </div>
      <div class="card">
        <div class="card-name">Accidente Inverso</div>
        <div class="card-desc">Se toma una excepción a una regla general y se aplica como si fuera la regla en todos los casos, generalizando indebidamente.</div>
        <span class="card-tag">→ Muestra que el caso especial es una excepción, no la norma</span>
      </div>
    </div>
  </div>

  <!-- 6. CAUSALES -->
  <div class="category cat-6">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Falacias Causales</div>
      <div class="category-count">05 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Correlación Coincidente</div>
        <div class="card-latin">post hoc ergo propter hoc</div>
        <div class="card-desc">"Después de esto, luego a causa de esto." Se asume que porque B ocurrió después de A, A causó B, confundiendo secuencia temporal con causalidad.</div>
        <span class="card-tag">→ El efecto habría ocurrido sin esa causa, o tiene otra</span>
      </div>
      <div class="card">
        <div class="card-name">Efecto Conjunto</div>
        <div class="card-desc">Se afirma que A causa B, cuando en realidad ambos son efectos de una causa subyacente común C que no se menciona.</div>
        <span class="card-tag">→ Describe la causa subyacente común</span>
      </div>
      <div class="card">
        <div class="card-name">Causa Genuina pero Insignificante</div>
        <div class="card-desc">La causa identificada es real pero trivial en comparación con otras causas mucho más relevantes del mismo efecto.</div>
        <span class="card-tag">→ Señala la causa significativa omitida</span>
      </div>
      <div class="card">
        <div class="card-name">Dirección Equivocada</div>
        <div class="card-desc">La relación causal se invierte: se identifica como causa lo que en realidad es el efecto, y viceversa.</div>
        <span class="card-tag">→ Demuestra que la dirección causa→efecto está invertida</span>
      </div>
      <div class="card">
        <div class="card-name">Causa Compleja</div>
        <div class="card-desc">El efecto tiene múltiples causas necesarias, pero se señala solo una de ellas como responsable, ignorando el resto del sistema causal.</div>
        <span class="card-tag">→ Muestra que todas las causas son necesarias, no solo una</span>
      </div>
    </div>
  </div>

  <!-- 7. PERDIENDO EL PUNTO -->
  <div class="category cat-7">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Perdiendo el Punto</div>
      <div class="category-count">03 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Suplicando la Pregunta</div>
        <div class="card-latin">petitio principii / razonamiento circular</div>
        <div class="card-desc">La conclusión ya está asumida, implícita o explícitamente, en las propias premisas. Probar algo con aquello que se quiere probar.</div>
        <span class="card-tag">→ Para creer las premisas, ya debes aceptar la conclusión</span>
      </div>
      <div class="card">
        <div class="card-name">Conclusión Irrelevante</div>
        <div class="card-latin">ignoratio elenchi</div>
        <div class="card-desc">El argumento prueba una conclusión diferente a la que pretendía probar, desviando el debate hacia otro punto sin advertirlo.</div>
        <span class="card-tag">→ La conclusión probada no es la que se propuso probar</span>
      </div>
      <div class="card">
        <div class="card-name">Hombre de Paja</div>
        <div class="card-desc">Se distorsiona o debilita el argumento del oponente para atacar esa versión falsa en lugar de su postura real y más sólida.</div>
        <span class="card-tag">→ Muestra el argumento más fuerte que fue ignorado</span>
      </div>
    </div>
  </div>

  <!-- 8. AMBIGÜEDAD -->
  <div class="category cat-8">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Falacias de Ambigüedad</div>
      <div class="category-count">02 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Equívoco</div>
        <div class="card-desc">Una misma palabra con dos significados distintos (polisemia) se usa en ambos sentidos dentro del mismo argumento, generando una conclusión inválida.</div>
        <span class="card-tag">→ Identifica la palabra y sus dos definiciones incompatibles</span>
      </div>
      <div class="card">
        <div class="card-name">Anfibología</div>
        <div class="card-desc">La construcción gramatical de una oración le permite tener dos interpretaciones diferentes, y se explota esa ambigüedad sintáctica.</div>
        <span class="card-tag">→ Muestra las dos lecturas posibles de la frase</span>
      </div>
    </div>
  </div>

  <!-- 9. ERRORES DE CATEGORÍA -->
  <div class="category cat-9">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Errores de Categoría</div>
      <div class="category-count">02 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Composición</div>
        <div class="card-desc">Porque las partes de un todo tienen una propiedad, se concluye que el todo también la tiene, confundiendo propiedades distributivas con colectivas.</div>
        <span class="card-tag">→ La propiedad pertenece al todo, no a cada parte</span>
      </div>
      <div class="card">
        <div class="card-name">División</div>
        <div class="card-desc">Porque el todo tiene una propiedad, se concluye que cada una de sus partes también la tiene. Error inverso a la composición.</div>
        <span class="card-tag">→ La propiedad del todo no se transfiere a sus partes</span>
      </div>
    </div>
  </div>

  <!-- 10. NON SEQUITUR -->
  <div class="category cat-10">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Non Sequitur</div>
      <div class="category-count">03 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Afirmando lo Consecuente</div>
        <div class="card-desc">Forma inválida: "Si A entonces B. B. Por lo tanto A." Que B sea verdadero no prueba que A fue su única causa posible.</div>
        <span class="card-tag">→ B podría ser consecuencia de algo distinto de A</span>
      </div>
      <div class="card">
        <div class="card-name">Negando el Antecedente</div>
        <div class="card-desc">Forma inválida: "Si A entonces B. No A. Por lo tanto no B." Que A sea falso no impide que B ocurra por otras razones.</div>
        <span class="card-tag">→ B puede ocurrir aunque A no ocurra</span>
      </div>
      <div class="card">
        <div class="card-name">Inconsistencia</div>
        <div class="card-desc">El autor sostiene dos o más proposiciones que no pueden ser todas verdaderas al mismo tiempo; son contradictorias o contrarias entre sí.</div>
        <span class="card-tag">→ Si una es verdadera, la otra debe ser falsa</span>
      </div>
    </div>
  </div>

  <!-- 11. SILOGÍSTICAS -->
  <div class="category cat-11">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Falacias Silogísticas</div>
      <div class="category-count">07 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Cuatro Términos</div>
        <div class="card-latin">quaternio terminorum</div>
        <div class="card-desc">Un silogismo válido requiere exactamente tres términos; cuando aparece una palabra con dos significados distintos, en realidad hay cuatro términos y el razonamiento es inválido.</div>
        <span class="card-tag">→ Identifica el término ambiguo que duplica los términos</span>
      </div>
      <div class="card">
        <div class="card-name">Medio No Distribuido</div>
        <div class="card-desc">El término medio del silogismo nunca cubre la totalidad de su categoría en ninguna de las premisas, por lo que no conecta los extremos de forma válida.</div>
        <span class="card-tag">→ Las dos categorías podrían ser grupos separados con propiedad común</span>
      </div>
      <div class="card">
        <div class="card-name">Mayor Ilícito</div>
        <div class="card-desc">El término mayor (predicado de la conclusión) se usa en sentido universal en la conclusión, pero en la premisa mayor solo abarca una parte de esa categoría.</div>
        <span class="card-tag">→ Hay miembros del término mayor que contradicen la conclusión</span>
      </div>
      <div class="card">
        <div class="card-name">Menor Ilícito</div>
        <div class="card-desc">El término menor (sujeto de la conclusión) se toma en sentido universal en la conclusión, pero en las premisas solo se refería a una parte de esa categoría.</div>
        <span class="card-tag">→ Hay miembros del término menor que contradicen la conclusión</span>
      </div>
      <div class="card">
        <div class="card-name">Premisas Exclusivas</div>
        <div class="card-desc">Ambas premisas del silogismo son negativas; con dos negaciones no se puede tender un puente lógico entre los términos para obtener ninguna conclusión válida.</div>
        <span class="card-tag">→ Dos negaciones no permiten ninguna conclusión</span>
      </div>
      <div class="card">
        <div class="card-name">Conclusión Afirmativa desde Premisa Negativa</div>
        <div class="card-desc">La conclusión es afirmativa cuando al menos una premisa es negativa; la negatividad de una premisa "impide" obtener una conclusión afirmativa válida.</div>
        <span class="card-tag">→ Con una premisa negativa, la conclusión debe ser negativa</span>
      </div>
      <div class="card">
        <div class="card-name">Falacia Existencial</div>
        <div class="card-desc">Con dos premisas universales se extrae una conclusión particular, asumiendo que los miembros de la categoría existen en la realidad, lo cual no está garantizado.</div>
        <span class="card-tag">→ Las premisas universales no garantizan existencia real de instancias</span>
      </div>
    </div>
  </div>

  <!-- 12. EXPLICACIÓN -->
  <div class="category cat-12">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Falacias de Explicación</div>
      <div class="category-count">05 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Soporte Subvertido</div>
        <div class="card-desc">Se ofrece una explicación de un fenómeno que en realidad no ocurre, o del que no hay evidencia de que suceda. Se explica lo inexistente.</div>
        <span class="card-tag">→ Demuestra que el fenómeno explicado no ha ocurrido realmente</span>
      </div>
      <div class="card">
        <div class="card-name">No Soporte</div>
        <div class="card-desc">El fenómeno existe, pero la evidencia que lo respalda está manipulada, es falsa, sesgada o fue construida ad hoc para sostener la explicación.</div>
        <span class="card-tag">→ Muestra que la evidencia fue fabricada o manipulada</span>
      </div>
      <div class="card">
        <div class="card-name">Inestabilidad</div>
        <div class="card-desc">La teoría propuesta no puede ser puesta a prueba, ya que no hace predicciones verificables o sus predicciones nunca podrían resultar falsas.</div>
        <span class="card-tag">→ La teoría no es falsificable ni hace predicciones comprobables</span>
      </div>
      <div class="card">
        <div class="card-name">Alcance Limitado</div>
        <div class="card-desc">La teoría solo explica el fenómeno puntual para el que fue diseñada y no puede aplicarse a ningún otro caso o fenómeno relacionado.</div>
        <span class="card-tag">→ La teoría no explica nada más allá de ese hecho puntual</span>
      </div>
      <div class="card">
        <div class="card-name">Profundidad Limitada</div>
        <div class="card-desc">La explicación no apela a una causa real subyacente; solo clasifica el fenómeno dentro de una categoría sin indagar en el porqué auténtico.</div>
        <span class="card-tag">→ Clasifica sin explicar la causa raíz del fenómeno</span>
      </div>
    </div>
  </div>

  <!-- 13. DEFINICIÓN -->
  <div class="category cat-1">
    <div class="category-header">
      <div class="category-dot"></div>
      <div class="category-title">Falacias de Definición</div>
      <div class="category-count">04 tipos</div>
    </div>
    <div class="grid">
      <div class="card">
        <div class="card-name">Demasiado Amplio</div>
        <div class="card-desc">La definición incluye elementos que no pertenecen al concepto; es tan vaga que cosas que no son del tipo quedan comprendidas en ella.</div>
        <span class="card-tag">→ Hay algo que cumple la definición pero no es instancia del término</span>
      </div>
      <div class="card">
        <div class="card-name">Demasiado Estrecho</div>
        <div class="card-desc">La definición excluye elementos que sí deberían pertenecer al concepto; es tan restrictiva que deja afuera instancias legítimas del término.</div>
        <span class="card-tag">→ Hay algo que es instancia del término pero no cumple la definición</span>
      </div>
      <div class="card">
        <div class="card-name">Falta de Aclaración</div>
        <div class="card-desc">La definición resulta más oscura o difícil de entender que el propio término que intenta definir; explica lo conocido con lo desconocido.</div>
        <span class="card-tag">→ Las condiciones de la definición son menos claras que el término</span>
      </div>
      <div class="card">
        <div class="card-name">Definición Circular</div>
        <div class="card-desc">El término que se define aparece dentro de la propia definición, ya sea de forma directa o como sinónimo, haciendo la definición inútil.</div>
        <span class="card-tag">→ El término definido aparece en sus propias condiciones definitivas</span>
      </div>
    </div>
  </div>

</div>

<footer>
  <p>FALACIAS LÓGICAS — 13 categorías · <span>46 tipos</span> · Referencia completa</p>
</footer>

</body>
</html>
