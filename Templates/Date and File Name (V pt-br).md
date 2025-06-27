<%*
// Línguagem potuguês (BR)
moment.locale("pt-br");

// Definição do nome do arquivo
let dateMonthNumerical = tp.file.creation_date("MM");
let dateMonthWritten = tp.file.creation_date("MMMM");

let monthWrittenWithCapOne = dateMonthWritten.charAt(0).toUpperCase() + dateMonthWritten.slice(1);
let fileName = dateMonthNumerical + " - " + monthWrittenWithCapOne;

await tp.file.rename(fileName);
%># Anotação Mensal - <% monthWrittenWithCapOne + ": " + tp.file.creation_date("YYYY", 0, tp.file.title, "YYYY") %>

