<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Akshat Raj – AI Engineer</title>

  <!-- SEO -->
  <meta name="description" content="AI Engineer, ML Developer, Founder – OnePersonAI" />
  <meta name="author" content="Akshat Raj" />
  <meta name="keywords" content="AI Engineer, Deep Learning, NLP, FastAPI, Next.js, OnePersonAI" />

  <style>
    body { font-family: Inter, sans-serif; background:#0d1117; color:#e6edf3; padding:40px; }
    h1, h2 { color:#58a6ff; }
    .section { margin-top:40px; }
    .card { background:#161b22; padding:20px; border-radius:10px; margin-bottom:15px; }
    .tag { background:#21262d; padding:4px 8px; border-radius:6px; margin-right:6px; font-size:12px; }
  </style>
</head>

<body>
<!-- ========================= -->
<!--        DATA BLOCK         -->
<!-- (JSON + YAML MIXED DATA) -->
<!-- ========================= -->

<script id="profile-data" type="application/json">
{
  "name": "Akshat Raj",
  "role": "AI Engineer",
  "founder": "OnePersonAI",
  "skills": {
    "ai": ["Machine Learning", "Deep Learning", "NLP", "Transformers", "PyTorch", "TensorFlow"],
    "backend": ["FastAPI", "Flask", "Node.js", "MongoDB"],
    "frontend": ["React", "Next.js", "TypeScript"],
    "cloud": ["AWS", "Vercel", "Render"]
  },
  "projects": [
    { "name": "Emotion Detection AI", "stack": ["TensorFlow", "NLP", "Python"] },
    { "name": "Heart Disease Prediction", "stack": ["Sklearn", "Streamlit"] },
    { "name": "AkshaBot", "stack": ["FastAPI", "NLP"] },
    { "name": "OnePersonAI Website", "stack": ["Next.js", "TailwindCSS"] }
  ]
}
</script>


<script id="profile-yaml" type="text/yaml">
name: "Akshat Raj"
title: "AI Engineer • ML Developer"
company: "OnePersonAI"
skills:
  ai:
    - Machine Learning
    - Deep Learning
    - NLP
    - Transformers
    - PyTorch
    - TensorFlow
  backend:
    - FastAPI
    - Flask
    - Node.js
    - MongoDB
  frontend:
    - React
    - Next.js
    - TypeScript
  cloud:
    - AWS
    - Vercel
    - Render

projects:
  - name: "Emotion Detection AI"
    tech: ["TensorFlow", "NLP", "Python"]

  - name: "Heart Disease Prediction"
    tech: ["Sklearn", "Streamlit"]

  - name: "AkshaBot"
    tech: ["FastAPI", "NLP"]

  - name: "OnePersonAI Website"
    tech: ["Next.js", "TailwindCSS"]
</script>

<!-- ========================= -->
<!--      REACT UI BLOCK      -->
<!-- ========================= -->

<div id="app"></div>

<script type="text/babel">
  const jsonData = JSON.parse(document.getElementById("profile-data").innerHTML);

  const App = () => (
    <div>
      <h1>{jsonData.name}</h1>
      <h2>{jsonData.role} • Founder – {jsonData.founder}</h2>

      <div className="section">
        <h2>Skills</h2>
        {Object.entries(jsonData.skills).map(([cat, list]) => (
          <div className="card" key={cat}>
            <strong>{cat.toUpperCase()}</strong><br /><br />
            {list.map(skill => <span key={skill} className="tag">{skill}</span>)}
          </div>
        ))}
      </div>

      <div className="section">
        <h2>Projects</h2>
        {jsonData.projects.map(p => (
          <div className="card" key={p.name}>
            <strong>{p.name}</strong><br /><br />
            {p.stack.map(s => <span key={s} className="tag">{s}</span>)}
          </div>
        ))}
      </div>
    </div>
  );

  ReactDOM.render(<App />, document.getElementById("app"));
</script>

<!-- React CDN -->
<script src="https://unpkg.com/react@17/umd/react.development.js"></script>
<script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
<script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

</body>
</html>
