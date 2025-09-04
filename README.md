# 🚀 FreeRDP Portable (Ubuntu amd64) FreeRDP version 3.17.2-dev0
- Puedes añadorlo a tus binarios para usarlo de manera global.
## 🔹 1. Estructura final del paquete
```
freerdp-portable/
 ├── xfreerdp
 └── lib/
     ├── libfreerdp-client3.so.3
     ├── libfreerdp-client3.so.3.17.2
     ├── libfreerdp3.so.3
     ├── libfreerdp3.so.3.17.2
     ├── libwinpr3.so.3
     └── libwinpr3.so.3.17.2
```

## 🔹 Guía


Este paquete incluye **FreeRDP version 3.17.2-dev0** ya compilado con todas las librerías necesarias.
No requiere instalación ni compilación.

## 🔹 Cómo usarlo

1. Descargar y descomprimir:

   ```bash
   unzip freerdp-portable-ubuntu-amd64.zip
   cd freerdp-portable
   ```

2. Ejecutar FreeRDP:

   ```bash
   LD_LIBRARY_PATH=$PWD/lib ./xfreerdp /version
   ```

3. Conectarse a un servidor RDP:

   ```bash
   LD_LIBRARY_PATH=$PWD/lib ./xfreerdp /v:IP_SERVIDOR /u:usuario /p:contraseña
   ```

---

## 🔹 (Opcional) Crear un alias para no escribir tanto

Ejecuta esto una sola vez:
o tu SHELL que estas usando.
```bash
echo "alias xfreerdp='LD_LIBRARY_PATH=$HOME/freerdp-portable/lib $HOME/freerdp-portable/xfreerdp'" >> ~/.bashrc
source ~/.bashrc
```

Ahora podrás usar:

```bash
xfreerdp /v:IP_SERVIDOR
```

---

## 🔹 Requisitos

* Ubuntu 20.04 o superior (amd64).
* En mi caso uso Ubuntu 24.04.3 LTS x86_64 (Recomendado)
* Librerías estándar del sistema (OpenSSL, X11, PulseAudio, etc.) que ya vienen con Ubuntu.
