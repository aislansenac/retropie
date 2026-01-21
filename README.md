# 🎮 RetroPie — Dicas e Configurações

## 🕹️ PlayStation

### 📦 Arquivo Necessário

- Certifique-se de ter o arquivo `SCPH1001.BIN` na pasta correta `/home/pi/RetroPie/roms/psx`.

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

# Atualizar localização 
# Configurar controle
# Inserir a Wi-Fi 
# Atualizar Rasp-config
# Atualizar retroarch
# Vídeo HDMI
# Subir jogos
# Botão Start
### @kitsune , acho que esse é o mesmo problema que tive recentemente. Tente desabilitar o "multitap". Inicie um jogo, acesse as configurações do Retroarch (selecione e execute na maioria das castas) e vá em "opções"... habilite "mostrar outras configurações de entrada". Saia do jogo e comece de novo. Volte para as opções e deve haver algumas configurações disponíveis. Duas delas são "multitap 1" e "multitap 2". Desative ambas e reinicie novamente. Isso resolveu o problema para mim.
### 
 29 de novembro de 2020, 19:26

@yelworc Muito obrigado! Tive o mesmo problema e tentei várias outras opções, sem sucesso.

Algumas pequenas correções em suas instruções:

O menu do RetroArch é acessado com a tecla de atalho + X por padrão, enquanto a maioria das pessoas define a tecla de atalho para Selecionar, então ela deve ser Selecionar + X na maioria das configurações.
Não é necessário reiniciar o jogo após habilitar Mostrar outras configurações de entrada. Basta retomar o jogo e entrar novamente no menu para ver as opções adicionais.
Depois de desabilitar os dois Multitaps, os botões Iniciar funcionaram como deveriam, embora eu também tenha precisado salvar uma Substituição de Núcleo (em Menu Rápido > Substituições) para fazer as alterações durarem.
Obrigado novamente por me apontar a direção certa!

@mitu Será que isso deveria ser o padrão no RetroPie? Parece um tanto estranho que as configurações padrão atuais Multitap 1 + 2 = Automático impeçam o botão Iniciar de funcionar, enquanto Mostrar Outras Configurações de Entrada = Desativado oculta essas opções simultaneamente do player.


Moderador Global
 30 de novembro de 2020, 01:51

@clyde Por padrão, as opções de Multitap estão desabilitadas e a opção " Mostrar Outras Configurações de Entrada" está desativada . Em algum momento, o Multitap foi definido como automático , mas agora não está mais . Acho que os usuários que atualizaram em algum momento receberam o padrão (na época), o que interrompeu a entrada. No entanto, agora, ao iniciar o Core pela primeira vez, as opções de Multitap estão desabilitadas.

### [https://retropie.org.uk/forum/topic/35590/when-i-click-the-start-button-on-my-controller-the-main-menu-only-has-sound-settings-and-quit?_=1745917978931](https://retropie.org.uk/forum/topic/28656/start-button-on-psx-emulator-doesn-t-work/4)
