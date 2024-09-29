
## Configuración de DNS (IPv4)

1. **Abrir la pestaña Desktop:**
   - En el servidor, abrir la pestaña `Desktop` y seleccionar `IP Configuration`.

2. **Configurar la IP de forma estática:**
   - Marcar la opción `Static`.

3. **Asignar los parámetros de red para DNS:**

   - **IP:** `X.X.X.10`
   - **Máscara:** `255.0.0.0`
   - **Gateway:** `X.X.X.1`
   - **Servidor DNS:** `X.X.X.10` *(la misma dirección IP del dispositivo, apuntando a sí mismo)*

---

## Configuración de servidores WEB (IPv4)

1. **Abrir la pestaña Desktop:**
   - En el servidor, abrir la pestaña `Desktop` y selecciona `IP Configuration`.

2. **Asignar los parámetros de red para WWW:**

   - **IP:** `50.0.0.20`
   - **Máscara:** `255.0.0.0`
   - **Gateway:** `50.0.0.1`
   - **Servidor DNS:** `X.X.X.10` *(servidor configurado previamente)*
