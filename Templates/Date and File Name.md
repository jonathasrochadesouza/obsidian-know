<%*
/*
Definição do nome do arquivo
*/

moment.locale("pt-br");

let dateMonthNumerical = tp.file.creation_date("MM");
let dateMonthWritten = tp.file.creation_date("MMMM");

let monthWrittenWithCapOne = dateMonthWritten.charAt(0).toUpperCase() + dateMonthWritten.slice(1);
let fileName = dateMonthNumerical + " - " + monthWrittenWithCapOne;

await tp.file.rename(fileName);
%><!-- Continuação Markdown --># Anotação Mensal - <% tp.file.creation_date("MMMM: YYYY", 0, tp.file.title, "YYYY-MM-DD-Mensal") %>

