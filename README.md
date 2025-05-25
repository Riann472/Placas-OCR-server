# Backend – Leitor de Placas Veiculares

Este é o backend da aplicação de leitura de placas de carros e motos, feito em **Node.js**. Ele recebe uma imagem via API, usa **Tesseract.js** para realizar OCR e retorna o texto detectado (possivelmente uma placa veicular).

---

## 🔧 Tecnologias Utilizadas

- Node.js
- Express
- Multer (upload de imagens)
- Sharp (processamento de imagens)
- Tesseract.js (OCR)
- Regex (detecção de padrão de placa)

---

## 🚀 Como rodar localmente

### 1. Clone este repositório

```bash
git clone https://github.com/seu-usuario/seu-repo-backend.git
cd seu-repo-backend
```

### 2. Instale as dependências

```bash
npm install
npm install -g nodemon
```
### 3. Configure as variaveis de ambiente .env
Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```env
PORT=3001
```
(Outras portas podem ser usadas tambem)

### 4. Inicie o servidor

```bash
npm run start
```

## 📡 Endpoint disponível

### `POST /upload`

- **Descrição:** Recebe uma imagem via `multipart/form-data`, aplica OCR e tenta extrair a placa.
- **Campo esperado:** `image`

#### 🧪 Exemplo de resposta:

```json
{"ABC1234"}
```

## 📌 Observações

- O Tesseract.js pode demorar alguns segundos para processar, dependendo da imagem.
- A acurácia da detecção melhora com imagens bem iluminadas e centralizadas.

> O backend estará disponível em [http://localhost:3001](http://localhost:3001)
