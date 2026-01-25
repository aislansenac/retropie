# 🎮 RetroPie — Dicas e Configurações

## ⚙️ Configuração Inicial do RetroPie (Primeiros Passos)

Antes de instalar jogos e configurar emuladores, é **muito importante ajustar o sistema** para evitar problemas futuros.

### 🛠️ Acessando o Raspi-Config

1. No menu principal do RetroPie, entre em **RetroPie**.
2. Selecione **raspi-config** e confirme com o botão **A**.

---

### 👤 Alterar Usuário e Senha

1. No **raspi-config**, entre em:
   - **1 System Options**
2. Altere:
   - Nome do usuário (se desejar)
   - Senha do usuário  

> 👉 Recomendado por segurança.

---

### 🌐 Habilitar Acesso Remoto (SSH)

1. Vá em:
   - **3 Interface Options**
2. Selecione:
   - **SSH**
3. Marque como **Enable**.

> 👉 Isso permite acessar o RetroPie remotamente pelo computador.

---

### 🌍 Configurações de Localização

Entre em:

- **5 Localisation Options**

Configure os itens abaixo:

#### 🗣️ Idioma do Sistema
- **L1 Locale**
- Marque:
  - `pt_BR.UTF-8 UTF-8`
- Defina como **padrão (Default)**.

#### ⏰ Fuso Horário
- **L2 Timezone**
- Selecione:
  - **America**
  - **Brazil**

#### 📡 País do Wi-Fi
- **L4 WLAN Country**
- Selecione:
  - **Brazil**

---

### ✅ Finalizar Configurações

- Selecione **Finish**
- Reinicie, se for solicitado.

---

### 📶 Ativar Wi-Fi no RetroPie

1. Volte ao menu **RetroPie**.
2. Entre em **WiFi**.
3. Configure sua rede sem fio.

---

### 🔄 Atualização do Sistema (Raspi-Config)

1. Retorne ao **raspi-config**.
2. Vá em:
   - **8 Update**
3. Aguarde a atualização finalizar.

---

### 🔧 Atualizar o RetroPie

1. No menu **RetroPie**, entre em **RetroPie-Setup**.
2. Execute:
   - **Update**
3. Em seguida:
   - **Update RetroPie-Setup script**
4. Após concluir, faça um **reboot** do sistema.

---

## ⚠️ RetroPie não inicia no modo gráfico?

Se, após reiniciar, o sistema **não entrar automaticamente na interface gráfica do RetroPie (EmulationStation)**, siga os passos abaixo:

### 🖥️ Ajustar Autostart do RetroPie

1. Acesse o terminal (localmente ou via SSH).
2. Digite o comando:

```bash
sudo ~/RetroPie-Setup/retropie_setup.sh
```

3. No menu que abrir, selecione:
   - **Configuration / tools**
4. Em seguida:
   - **autostart**
5. Escolha a opção para iniciar o **1 Start EmulationStation at boot**.
6. Saia do menu e reinicie o sistema.
> 👉 Isso garante que o RetroPie sempre inicie no modo gráfico.

---

## 🖥️ Remover Textos da Inicialização do RetroPie (Boot Clean)

Durante a inicialização do RetroPie, podem aparecer **mensagens de texto do sistema (boot messages)** antes de entrar no EmulationStation.  
É possível ocultar essas mensagens para deixar o boot mais limpo e visualmente agradável.

### ⌨️ Acessar o Terminal no RetroPie

1. Na tela inicial do RetroPie, pressione:
   - **F4**
2. Você será direcionado para o **terminal do sistema**.
---
### ✏️ Editar Arquivo de Inicialização

No terminal, digite o comando abaixo:

```bash
sudo nano /boot/cmdline.txt
```
> ⚠️ Atenção:
Este arquivo deve permanecer em apenas uma linha.
Não pressione Enter dentro dele.
---
### 🔎 Alterar o Console Padrão

* Arquivo original:
```text
console=serial0,115200 console=tty1 root=PARTUUID=00f2345f-02 rootfstype=ext4 fsck.repair=yes rootwait loglevel=3 consoleblank=0 plymouth.enable=0
```
* Meu arquivo *cmdline.txt*, ficou assim:
```text
console=tty10 root=PARTUUID=00f2345f-02 rootfstype=ext4 fsck.repair=yes rootwait quiet loglevel=0 consoleblank=0 plymouth.enable=0 vt.global_cursor_default=0
```
O que cada opção faz:
* `console=tty10` → oculta mensagens do console principal
* `quiet` → reduz mensagens do kernel
* `loglevel=0` → remove logs do boot
* `vt.global_cursor_default=0` → remove o cursor piscando
* `console=serial0,115200 (opcional)`  → Mantém logs na porta serial (HDMI não mostra) pode manter, não atrapalha o visual

Se quiser silêncio absoluto até na serial, pode remover
> 👉 Isso faz com que as mensagens do sistema sejam enviadas para outro terminal, ficando ocultas da tela principal.
---
### 💾 Salvar e Sair

No editor nano:
* Pressione CTRL + O → Enter (salvar)
* Pressione CTRL + X (sair)
---
### 🔄 Reiniciar o Sistema

Para aplicar as alterações, reinicie o sistema:
```text
sudo reboot
```
Após reiniciar, o RetroPie iniciará com a tela mais limpa, sem as mensagens de texto durante o boot 🎮✨

---

## 🕹️ PlayStation

### 📦 Arquivo Necessário

- Certifique-se de ter o arquivo `SCPH1001.BIN` na pasta correta `/home/pi/RetroPie/BIOS`.

### 🎮 Ativar Vibração do Controle

1. Durante o jogo, pressione `HotKey + X`.
2. Vá em **Menu Rápido** → **Controles**.
3. Selecione **Controle da porta 1**.
4. Em **Tipo de dispositivo**, escolha `dualshock`.
5. Reinicie o jogo para aplicar.

---

## 🐉 Neo Geo

### 📦 Arquivo Necessário

- Certifique-se de ter o arquivo `neogeo.zip` na pasta correta `/home/pi/RetroPie/roms/neogeo`.

### ⚙️ Configurar para Praticar

1. Durante o jogo, pressione `HotKey + X`.
2. Vá em **Menu Rápido** → **Configurações do Núcleo**.
3. Em **Diagnostic Input**, configure para `Hold Start + L + R`.  
   _👉 Isso evita que fique entrando nessa tela sem querer._
4. Em **Neo-Geo Settings**, configure:
   - `NeoGeo Mode` → `UNIBIOS`
5. Reinicie o jogo.

### 🎛️ Configuração de Teclas

- **1.** Tecla **B** → A  
- **2.** Tecla **A** → B  
- **3.** Tecla **Y** → C  

### 🌍 Configurar Região e Modo

1. Pressione `A + B + C` juntos.
2. Selecione **Region Setup** (pressione A).
3. Escolha:
   - **Region:** `-----`
   - **Mode:** `Console`

---

✅ Pronto! Agora você está com tudo configurado para aproveitar ao máximo.
