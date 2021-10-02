# Crear proyecto usando el GitHub Flow

## Prequisitos: 

* Crear repositorio en GitHub
* Opcional: crear proyecto Kanban en repositorio, TODO:
  - [APP] Crear TopBar
  - [CICD] Crear workflows
  - [APP] Crear SimpleContainer

### 1. Crear nueva rama 
Usar un nombre descriptivo, ejemplo: crear-navbar

### 2. Crear archivos y agregar commits
Crear archivo `touch src/containers/TopBar/TopBar.js` y agregar: 

```
import * as React from 'react';
import AppBar from '@mui/material/AppBar';
import Box from '@mui/material/Box';
import Toolbar from '@mui/material/Toolbar';
import Typography from '@mui/material/Typography';
import GitHubIcon from '@mui/icons-material/GitHub';

export default function TopBar() {
  return (
    <Box sx={{ flexGrow: 1 }}>
      <AppBar position="static" color="secondary">
        <Toolbar variant="dense">
          <Typography variant="h6" color="inherit" component="div">
            GitHub Flow Demo 
          </Typography>
          <GitHubIcon edge="end"/>
        </Toolbar>
      </AppBar>
    </Box>
  );
}
```

En `app.js`

```
import './App.css';
import TopBar from './containers/TopBar/TopBar.js';

function App() {
  return (
    <div className="App">
      <TopBar></TopBar>
    </div>
  );
}

export default App;
```

Mensajes claros. "Con este commit..."

### 3. Abrir pull request 

Push la rama desde VS Code. 

### 4. Discutir y revisar el codigo

Opcional: Asignar el PR y asociarle una issue del proyecto.

### 5. Merge

Opcional: borrar la rama.

### 6. Crear nueva rama, agregar CI/CD, PR y merge 
Usar un nombre descriptivo, ejemplo: crear-cicd

```
mkdir -p .github/workflows
touch .github/workflows/ci.yaml`
touch .github/workflows/cd.yaml
```

### 7. Agregar nuevos cambios
Crear archivo `touch src/containers/SimpleContainer/SimpleContainer.js` y agregar: 

```
import * as React from 'react';
import CssBaseline from '@mui/material/CssBaseline';
import Container from '@mui/material/Container';

export default function SimpleContainer() {
  return (
    <React.Fragment>
      <CssBaseline />
      <Container maxWidth="sm">
        <h1>Hola Mundo 2</h1>
      </Container>
    </React.Fragment>
  );
}
```

En `app.js`

```
import './App.css';
import TopBar from './containers/TopBar/TopBar.js';
import SimpleContainer from './containers/SimpleContainer/SimpleContainer';

function App() {
  return (
    <div className="App">
      <TopBar></TopBar>
      <SimpleContainer></SimpleContainer>
    </div>
  );
}

export
