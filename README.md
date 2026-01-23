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
5. Escolha a opção para iniciar o **EmulationStation automaticamente**.
6. Saia do menu e reinicie o sistema.
> 👉 Isso garante que o RetroPie sempre inicie no modo gráfico.

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


### [https://retropie.org.uk/forum/topic/35590/when-i-click-the-start-button-on-my-controller-the-main-menu-only-has-sound-settings-and-quit?_=1745917978931](https://retropie.org.uk/forum/topic/28656/start-button-on-psx-emulator-doesn-t-work/4)
