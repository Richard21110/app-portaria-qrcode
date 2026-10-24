# 🚪 App Controle de Acesso & Portaria (QR Code)

Aplicativo mobile corporativo desenvolvido em React Native (Expo) para controle e validação de acessos na portaria via leitura de QR Code no modelo **Operador-scans-User**.

---

## 📁 Estrutura de Pastas do Projeto

```text
meu-aap-portaria/
├── assets/                 # Arquivos estáticos (imagens, ícones e fontes)
├── src/                    # Código fonte do aplicativo
│   ├── components/         # Componentes visuais reutilizáveis (botões, cards, inputs)
│   ├── config/             # Arquivos de configuração global (ex: firebase.js)
│   ├── navigation/         # Configuração de rotas e navegação entre telas
│   └── screens/            # Telas do aplicativo
│       ├── RegisterScreen.js # Tela de cadastro dos dados do usuário
│       ├── QRCodeScreen.js   # Tela do crachá digital (gera o QR Code)
│       ├── ScannerScreen.js  # Tela do operador (lê o QR Code via câmera)
│       └── LogsScreen.js     # Painel de histórico de acessos em tempo real
├── App.js                  # Ponto de entrada principal da aplicação
├── app.json                # Configurações do ecossistema Expo e permissões
└── package.json            # Gerenciador de dependências e scripts do projeto
🛠️ Comandos de Instalação de Dependências
Caso esteja configurando o projeto do zero ou clonando o repositório, rode os comandos no terminal dentro da pasta raiz:

1. Criar o Projeto Base com Expo
Bash
npx create-expo-app@latest . --template blank
2. Instalar o Firebase (Backend & Firestore)
Bash
npx expo install firebase
3. Instalar Câmera e Gerador/Leitor de QR Code
Bash
npx expo install react-native-qrcode-svg react-native-svg expo-camera
4. Instalar o Sistema de Navegação (React Navigation)
Bash
npx expo install @react-navigation/native @react-navigation/native-stack react-native-screens react-native-safe-area-context
🚀 Como Rodar o Projeto
Instalar dependências (caso tenha acabado de clonar o repositório):

Bash
npm install
Configurar as Chaves do Firebase:
Abra o arquivo src/config/firebase.js e adicione as credenciais do seu console do Firebase:

JavaScript
const firebaseConfig = {
  apiKey: "SUA_API_KEY",
  authDomain: "SEU_PROJECT_ID.firebaseapp.com",
  projectId: "SEU_PROJECT_ID",
  storageBucket: "SEU_PROJECT_ID.appspot.com",
  messagingSenderId: "SEU_SENDER_ID",
  appId: "SEU_APP_ID"
};
Iniciar o Servidor de Desenvolvimento:

Bash
npx expo start
