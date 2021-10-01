# Crear proyecto usando el GitHub Flow
Crear proyecto usando el GitHub Flow

Prequisitos: Crear repositorio en GitHub

### 1. Crear nueva rama 
Usar un nombre descriptivo, ejemplo: create-navbar

### 2. Agregar commits
Crear archivo `src/containers/ButtonAppBar/ButtonAppBar.js` y agregar: 

```
import * as React from 'react';
import AppBar from '@mui/material/AppBar';
import Box from '@mui/material/Box';
import Toolbar from '@mui/material/Toolbar';
import Typography from '@mui/material/Typography';
import Button from '@mui/material/Button';
import IconButton from '@mui/material/IconButton';
import MenuIcon from '@mui/material/Menu';

export default function ButtonAppBar() {
  return (
    <Box sx={{ flexGrow: 1 }}>
      <AppBar position="static">
        <Toolbar>
          <IconButton
            size="large"
            edge="start"
            color="inherit"
            aria-label="menu"
            sx={{ mr: 2 }}
          >
            <MenuIcon />
          </IconButton>
          <Typography variant="h6" component="div" sx={{ flexGrow: 1 }}>
            Hola Mundo
          </Typography>
          <Button color="inherit">Login</Button>
        </Toolbar>
      </AppBar>
    </Box>
  );
}
```

En `app.js`

```
import './App.css';
import ButtonAppBar from './containers/ButtonAppBar/ButtonAppBar.js';

function App() {
  return (
    <div className="App">
      <ButtonAppBar></ButtonAppBar>
    </div>
  );
}

export default App;
```

Mensajes claros. "Con este commit..."

### 3. Abrir pull request 
### 4. Discutir y revisar el codigo
### 5. Despleguar 
Usar CI/CD
### 6. Merge
