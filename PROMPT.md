Generate a modern Single Page Application. Follow the requisites:

# General requisites:

- All application needs to work on frontend using HTML, CSS and Javascript.
- Don't use frameworks like Angular, React or Vue.
- Always use beautiful fonts for web like Roboto, Helvetica, etc. Do not use fonts that diverge from Material UI Design.
- Always use free icons libraries like Material Symbols, Font Awesome, Bootstrap Icons, etc.
- By default the application will use brazilian portuguese language.
- Use a responsive layout to work on both desktop and mobile.
- The application needs to be a feature to enable and disable dark mode.

## Template Main Page

- Needs to have a toolbar on top this page with a sandwich menu button to show and hide side nav bar.
- The top toolbar needs to have the name of application: Gerador de Carta de Oposição Claude.
- This page need to have a sidenav for nagivate to others pages.
- A main content with show all others pages that exists in this app.

## Home Page

- This page will have a jumbotron to welcome visitors.

## PDF Form Generator Page

- This page will have a form with the follows inputs:
    - Sindicato (input text. Default Value: SINDPD-CE)
    - Nome Completo (input text)
    - Carteira Profissional (input text)
    - Nome da Empresa (input text)
    - CNPJ (input text)
    - Endereço (input text)
    - Bairro (input text)
    - Cidade (input text)
    - Estado (input text)
    - Cidade de envio (input text)
    - Data de envio (input date)
- All the fields are required and need to be filled.
- Read the attached xml file for create the fields and coding to replace pattern of this file.
- Create a variable in the code where I can paste all the content from the xml. For example: const templateXml = `PLACE YOUR CODE HERE`;
- The inputs of the form will be filled the embedded file using the pattern. For example: #FIELD_NAME# where FIELD_NAME is the name of the field in upper snake case.
- The date field "Data de envio" need to be formatted as "28 de fevereiro de 2024".
- Its need a button "Gerar PDF" to send the embeded file as a multipart/form-data to the follow external api: https://libreoffice-to-pdf.vercel.app/api/upload
- This external api only accept form-data with name "file".
- The button "Gerar PDF" will open a new tab to proccess the external api link. Don't use fetch api, use hidden forms to avoid CORS policy.