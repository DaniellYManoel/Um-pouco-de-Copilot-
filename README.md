# Reconhecimento de texto em imagens

O projeto de hoje é cosiguir estrair o texto de algumas imagem, com ajuda do copilot.

### Introdução 
Eu perdi que o copilot gerasse algumas imagens e depois perdi que ele me auxiliasse a estrair os texto da imagens que ele gerou.  
As imagens que foram gerada está no pasta 'inputs', e o texto estraido estão na pasta 'output' ambas nesse repositorio.

### Desenvolvimento
Este foi o meu primeiro prompt utilizado: "crie outra imagem que eu possa utilizar no meu projeto de reconhecimento de texto nessas imagens."
![_3076d607-52c3-4f84-ba15-a421199b2a57](https://github.com/user-attachments/assets/8f87f005-ce3e-44f9-905d-887d457b05b7)
![_2b3a7e7b-6654-4304-aaed-4fae74ec6507](https://github.com/user-attachments/assets/81bdd36b-4da3-44da-81c0-b7d69f2a5155)

Que gerou está imagens. Não gostei muito das imagem, por que o texto está inlegível, então perdir pra que gera-se outras.

Segundo prompt: "com textos mais facil de ser indentificados"

![_9d89fb1f-7740-4631-bc16-2fb4e53c9a25](https://github.com/user-attachments/assets/0b2f49cf-8447-41a1-b335-d5ee45595c9d)
![_4954448f-f2fa-43ea-a566-f34902c748a6](https://github.com/user-attachments/assets/ffd9f664-d74b-48f8-b471-a37375fca88e)
![_25a95a21-fe38-46b1-ba63-677dd2e3cc67](https://github.com/user-attachments/assets/ba7d2150-4b28-46d0-aca7-8790c77c1136)
![_02dbe691-4a06-4ab2-8eaa-10471af8642e](https://github.com/user-attachments/assets/350c9e6f-3232-485f-91fe-1502d49166b5)


### Extração do texto

Para a estração do texto eu realizei este prompt: "como realiza o reconhecimento de texto dessa imagem"
Ele deu 2 opções.

##### 1 opção: Passos para Reconhecimento de Texto com Python e Tesseract

- Instalar as Bibliotecas Necessárias:
Primeiro, você precisa instalar o Tesseract e a biblioteca pytesseract no Python. Você também precisará do OpenCV para manipulação de imagens.

-> pip install pytesseract opencv-python

- Instalar o Tesseract:
Baixe e instale o Tesseract OCR.

- Código para Reconhecimento de Texto:
Aqui está um exemplo de código em Python para realizar o reconhecimento de texto em uma imagem:

=====================================================================================================

import cv2
import pytesseract

#Configurar o caminho do Tesseract

pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'

#Carregar a imagem

image = cv2.imread('caminho/para/sua/imagem.png')

#Converter a imagem para escala de cinza

gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

#Aplicar um limiar para binarizar a imagem

_, binary_image = cv2.threshold(gray, 150, 255, cv2.THRESH_BINARY)

#Usar o Tesseract para realizar o OCR

text = pytesseract.image_to_string(binary_image, lang='por')

#Exibir o texto reconhecido
print(text)

=====================================================================================================
#### Explicação do Código:
Importar Bibliotecas: Importamos cv2 para manipulação de imagens e pytesseract para OCR.
Configurar o Caminho do Tesseract: Definimos o caminho onde o Tesseract está instalado.
Carregar a Imagem: Carregamos a imagem que queremos processar.
Converter para Escala de Cinza: Convertendo a imagem para escala de cinza para facilitar o processamento.
Binarizar a Imagem: Aplicamos um limiar para binarizar a imagem, o que ajuda a melhorar a precisão do OCR.
Realizar OCR: Usamos pytesseract.image_to_string para extrair o texto da imagem.
Exibir o Texto: Finalmente, exibimos o texto reconhecido.

#### 2 Opção: O site image to text
Link do site que eu utilizei: https://www.imagetotext.io/pt Converter Imagem em Texto - Extrair Texto de Imagem (imagetotext.io)


## Finalização 
Foi esté o meu projeto do curso da DIO. Foi bem simples para mostrar um das muitas funcionalidade do copilot!
















