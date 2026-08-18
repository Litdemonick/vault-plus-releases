<div align="center">

# Vault+

**Tu gestor de contraseñas, cifrado de punta a punta.**
Para Windows y Android.

[![Descargar](https://img.shields.io/badge/Descargar-última_versión-6C63FF?style=for-the-badge)](https://github.com/Litdemonick/vault-plus-releases/releases/latest)

[![Windows](https://img.shields.io/badge/Windows-10_y_11-0078D4?logo=windows&logoColor=white)](https://github.com/Litdemonick/vault-plus-releases/releases/latest)
[![Android](https://img.shields.io/badge/Android-8.0+-3DDC84?logo=android&logoColor=white)](https://github.com/Litdemonick/vault-plus-releases/releases/latest)

</div>

---

## Qué es

Vault+ guarda tus contraseñas cifradas en **tu** dispositivo. La contraseña maestra —la que abre todo— nunca sale de ahí: no se envía, no se guarda en ningún servidor, y no existe ningún sitio desde donde se pueda recuperar.

Eso tiene una consecuencia que conviene entender antes de empezar: **si la olvidás, nadie puede devolvértela.** Ni vos, ni yo. Es el precio de que nadie más pueda abrir tu vault, y es exactamente lo que hace que valga la pena.

## Descargar

Todo está en la **[página de releases](https://github.com/Litdemonick/vault-plus-releases/releases/latest)**.

| Sistema | Archivo | Requisitos |
|---|---|---|
| **Windows** | `VaultPlus-<versión>-windows-setup.exe` | Windows 10 u 11, 64 bits |
| **Android** | `VaultPlus-<versión>-android.apk` | Android 8.0 o superior |

## Instalar

**Windows** — ejecutá el `.exe`. Se instala en tu carpeta de usuario, sin pedir permisos de administrador. Podés elegir otra carpeta durante la instalación.

**Android** — abrí el `.apk`. Android te va a advertir que viene de fuera de Play Store; es normal para una app que se distribuye así.

## Actualizar

**No desinstales la versión anterior.** Instalá la nueva encima:

- En **Windows**, el instalador detecta que ya lo tenés, actualiza en la misma carpeta y cierra la app solo si está abierta.
- En **Android**, el sistema reemplaza la app y conserva los datos.

En los dos casos **tu vault, tus ítems y tu contraseña maestra quedan intactos**. Desinstalar primero sí borra todo, así que no lo hagas salvo que esa sea la intención.

La app avisa sola cuando hay una versión nueva, y podés comprobarlo cuando quieras desde **Ajustes → Información → Buscar actualizaciones**. Si preferís que no revise sola, el interruptor está justo debajo.

## Verificar la descarga

Cada release trae un `SHA256SUMS.txt` con la huella de cada archivo. No hay una tienda de por medio comprobándolos, así que la comprobación es tuya:

```powershell
Get-FileHash .\VaultPlus-1.0.0-windows-setup.exe -Algorithm SHA256
```

Si el resultado no coincide con el del archivo, **no lo instales**.

## Licencia de uso

Vault+ se activa por equipo. Descargarlo no alcanza: hace falta una clave de acceso firmada.

1. Instalá la app y abrila.
2. Te va a mostrar el **código de tu equipo** (`VP-XXXX-XXXX-…`).
3. Envialo a quien te dio el acceso.
4. Pegá la clave que te devuelva.

Cada clave sirve para **un solo equipo**. Si cambiás de computadora o de teléfono, hace falta una nueva para ese equipo.

## Si algo va mal

Abrí un **[issue](https://github.com/Litdemonick/vault-plus-releases/issues)** contando qué pasó, en qué pantalla y en qué sistema.

> **Nunca** incluyas contraseñas, tu contraseña maestra, ni capturas con el vault abierto. Si el problema es de seguridad, escribime en privado en lugar de abrir un issue.

## Preguntas que aparecen siempre

<details>
<summary><b>¿Puedo recuperar mi contraseña maestra si la olvido?</b></summary><br>

No, y eso es a propósito. Tu vault está cifrado con una clave derivada de esa contraseña, y esa clave no está guardada en ningún lado. Sin la contraseña no hay nada que descifrar.

La red de seguridad es el **backup**: un archivo cifrado con su propia contraseña que podés guardar aparte. Creá uno desde Ajustes.
</details>

<details>
<summary><b>¿Mis contraseñas van a algún servidor?</b></summary><br>

No. Lo único que sale del dispositivo es la clave de tu vault **ya cifrada** bajo tu contraseña maestra, y sirve para que puedas entrar desde otro dispositivo con esa misma contraseña. Sin ella, ese dato no abre nada.

La sincronización entre tus dispositivos va **directa entre ellos** por tu red local, sin pasar por ningún servidor.
</details>

<details>
<summary><b>¿Qué pasa si pierdo el teléfono?</b></summary><br>

Quien lo tenga necesita tu contraseña maestra para abrir el vault. Podés además cambiar la contraseña de tu cuenta, lo que cierra la sesión en todos los dispositivos en menos de diez segundos.
</details>

<details>
<summary><b>¿Por qué este repositorio no tiene el código?</b></summary><br>

El código es privado. Acá solo se publican los instaladores, para que la app pueda comprobar si hay versiones nuevas sin que tengas que iniciar sesión en ningún lado.
</details>

---

<div align="center">
<sub>Carlos Miranda · <a href="https://github.com/litdemonick">@litdemonick</a></sub>
</div>
