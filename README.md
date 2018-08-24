# FCamara-FrontEnd

<h2>1) Se você tivesse 5 diferentes arquivos de folhas de estilo, qual seria a melhor forma de integrá-los no site?</h2>
<p>Para evitar a declaração de várias tags “link” dentro da tag “head”, que referencia os arquivos css:
<link rel=”stylesheet” type=”text/css” href=”arquivo1.css”>, a melhor técnica é utilizar um único arquivo CSS minificado, isto não só reduz o tamanho dos mesmos como diminui as requisição HTTP para baixar os arquivos, tornando o site mais rápido.
Ferramentas de automação, como o Gulp e Grunt, podem ser utilizadas para geração de um arquivo compacto, técnica conhecida como “minificação”.</p>

<h2>2) Fale 3 formas de diminuir o page load (tempo de carregamento real e percebido).</h2>
<p>Uma das causas mais comuns de tempo excessivo no carregamento de páginas web, se dá pela má organização das referências aos arquivos estáticos, tais como funções e chamadas de APIs externas, uma vez que a velocidade na renderização da página é afetada por aguardar a conclusão do processamento de tais arquivos.
<p>Dito isto, a primeira técnica seria deixar chamadas a arquivos javascript no fim da página, desta forma todos os componentes de visualização seriam concluídos primeiro. </p>
<p>A segunda técnica, seria utilizar ferramentas de compressão de arquivos CSS e/ou JS por exemplo, transformando-os em um único arquivo (minificação), desta forma menos requisições HTTP seriam efetuadas.</p>
<p>A terceira técnica se trata da redução do uso excessivo de imagens e vídeos pesados, além de possibilitar o armazenamento de tais arquivos em cache, desta forma o usuário não precisaria realizar o download novamente.</p> 

<h2>3) Quais ferramentas você usa para testar a performance do seu código?</h2>
<p>Uma abordagem inicial é verificar o tempo de execução de funcionalidades e módulos, afim de garantir sempre o menor tempo possível de execução, muitas linguagens disponibilizam técnicas de timestamp que podem ser utilizadas para tal analise. </p>
<p>Protractor para automação de testes, principalmente de páginas web.</p>
<p>JUnit, para testes unitários em códigos Java</p>
<p>Google PageSpeed para testes de varredura completa do site afim de descobrir lentidão</p>
<p>W3C validator para percentual de erros na página</p>

<h2>4) Considere o HTML5 como uma plataforma web aberta. Quais são os blocos de construção de HTML5?</h2>
<p>Muitos recursos novos foram adicionas no HTML5, como elementos HTML semânticos, elementos visuais, elementos de mídia e APIs. Para <p>definir um aquivo como HTML5, basta no inicializar o documento com a tag <!DOCTYPE html></p>
<p>Elementos semânticos: header, nav, main, section, aside, footer  </p>
<p>Elementos visuais: canvas, svg, drag & drop</p>
<p>Elementos de mídia: mídia, vídeo, áudio, plugins</p>
<p>APIs: Geolocalization, WebStorage, IndexedDB, WebWorkers, File</p>   

<h2>5) Você pode explicar a diferença entre GET e POST?</h2>
<p>Ambos são métodos HTTP que servem para trafegar informação na web, a diferença principal dos dois está na segurança e visibilidade das informações. O GET envia pequenas quantidades de informação, uma vez que há um limite de caracteres, estes dados são trafegas através da própria URL, que por sua vez não tem segurança, por exemplo: http://cantor.com.br/index.php?cd=1&musica=2 (deseja acessar a música 2 do CD 3).</p>
<p>Já o POST encapsulamento as informações no corpo da requisição HTTP, o que o torna mais seguro, não há limites de tamanho. Ele é mais lento que o GET, pois precisa encapsular as informações.</p>

<h2>6) Liste quantas propriedades display você puder lembrar.</h2>
<p>block</p>
<p>inline</p>
<p>inline-block</p>
<p>flex</p>
<p>grid</p>
<p>table</p>

<h2>7) Qual a diferença entre inline e inline-block?</h2>
<p>A diferença básica entre os dois, é que o inline é um tipo de elemento ao qual não é possível atribuir estilos de tamanho, margem e espaçamento, ou seja, ele ocupará na tela somente o espaço necessário para seu conteúdo. Já o inline-block, apesar de ter a mesma característica do inline, se posicionado lado a lado com outros do mesmo tipo, este pode receber estilização css.</p>

<h2>8) Qual a diferença entre elementos posicionados de forma relativa, fixa, absoluta e estática?</h2>
<p>OS elementos HTML são posicionados na tela seguindo uma determinada configuração de estilo, por padrão ele já vem na posição estática, ou seja, segue o fluxo normal da página. Relative possibilita a definição de valores de posicionamento como top, right, left e bottom, desta forma o elemento não estará restrito ao fluxo da página podendo até sobrepor outros elementos. A posição absoluta, semelhante ao relativo, entretanto seu posicionamento inicial começa a partir de seu elemento pai, por último o posicionamento fixo permite que o elemento seja posicionado em relação a tela, ou seja, mesmo que a página se mova através de uma barra de rolagem o elemento continuará fixo na posição definida.</p>

<h2>9) Qual a diferença entre .call e .apply?</h2>
<p>São protótipos já definidos para qualquer function javascript, ambos têm o objetivo de emprestar um método, entretanto o “apply” invoca uma função com o this e um array com o parâmetros da função, já o “call”, invoca o mesmo this, o os parâmetros da função, sem array. Por exemplo:</p>
<p>APPlY(contexto, array[param1, param2, ...])</p>
<p>CALL(contexto, param1, param2, ...)</p>

<h2>10) Qual a diferença entre == e ===?</h2>
<p>Ambos os casos tem o objetivo de verificar igualdade de resultados, com a ressalva que o === (3 iguais) garante também a igualdade dos tipos de dados das variáveis comparadas</p>
<p>Por exemplo, numa linguagem fracamente tipada, a comparação ‘10’ == 10 (string e inteiro), resultaria no valor verdadeiro, entretanto se a mesma for exposta a ’10’ === 10, resultará o valor false, pois ambas possuem tipos de dados diferentes.</p>
