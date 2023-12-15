<script>
  import Section from "../components/Section.svelte";
  import { onMount, tick } from "svelte";
  import ImageBanner from "../components/ImageBanner.svelte";
  import { slide, fade, blur } from "svelte/transition";
  import * as animateScroll from "svelte-scrollto";
  import { content } from "../utils/content";

  const section = content["sala5"];
  let element;
  let sound;
  onMount(() => {
    sound.play();
    animateScroll.scrollTo({
      element: "#scrollable",
      duration: 2000,
      delay: 400,
    });
  });
</script>

<div in:fade={{ duration: 1000 }} class="bg-[#29253d]">
  <audio src="./images/sala5/som.m4a" preload="auto" loop bind:this={sound}>
    <track kind="captions" />
  </audio>
  <Section {section} />
  <div id="scrollable" class="bg-[#29253d] h-full">
    <div class="text-white">
      <div class="px-5 flex flex-col items-center h-screen-80">
        <h2
          class="transition delay-50
            text-5xl tracking-wide font-quickbold py-10"
        >
          Acervo
        </h2>

        <!-- <div>Icons made by <a href="https://www.flaticon.com/authors/ilham-fitrotul-hayat" title="Ilham Fitrotul Hayat">Ilham Fitrotul Hayat</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/pixel-perfect" title="Pixel perfect">Pixel perfect</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div><div>Icons made by <a href="https://www.flaticon.com/authors/bomsymbols" title="BomSymbols">BomSymbols</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div> -->
        <div class="w-2/3 justify-center">
          <h2 class="text-3xl tracking-wide font-quickbold py-10 text-center">
            Imagens
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              wrapper="col-span-2"
              title="Quem tem medo de macumba?"
              data="sala5/quem_tem_medo.jpg"
            >
              <p slot="text">
                Em "Quem tem medo de macumba?", Pai Rodney relembra os
                ensinamentos da avó, Dona Aparecida: “Não mexa, não pegue nada
                nem pise. Antes de passar, peça licença e não olhe para trás.”
                Quando dizíamos que tínhamos visto uma “macumba”, ela
                imediatamente nos corrigia: “Uma entrega, meu filho”. Foto:
                Fernanda Procópio <a
                  href="https://www.flickr.com/photos/fernandaprocopio/7104086425/in/album-72157629513462180/"
                  >Link
                </a>  Instrumento musical muito antigo, macumba era parecido com
                um reco-reco, Macumbeiro, esclarece Pai Rodney de Oxóssi, era
                aquele que sabia tocá-lo. Na infância, a avó do também
                antropólogo, babalorixá e doutor em Ciências Sociais, Dona
                Aparecida, evitava o termo. Mais tarde ele descobriria que a
                expressão usada genericamente para referir-se às religiões
                afro-brasileiras tinha uma conotação pejorativa. "Era usada como
                sinônimo de feitiço, malefício ou bruxaria, por isso que vovó o
                evitava." Em Quem tem medo de macumba?, artigo escrito para a
                revista Capital em 2018, ele descreve práticas e crenças de
                longa data, trazendo memórias e relatos de quando criança.
              </p>
            </ImageBanner>
            <ImageBanner title="Macumba" data="sala5/macumba.jpg">
              <p slot="text">
                Do quimbundo, ma'kôba, macumba é uma árvore e um instrumento de
                percussão de origem africana. Utilizado em cerimônias de
                religiões afro-brasileiras, como o candomblé e a umbanda,
                macumba é desses nomes enfeitiçados. Variante do candomblé que
                só existe no Rio de Janeiro, ma cum ba, além de transfigurar-se
                de árvore e de música, passou a vestir-se de preconceito no
                início do século XX, quando igrejas neopentecostais e alguns
                outros grupos cristãos taxaram como profanas práticas de
                religiões que não fossem as suas. As africanas principalmente.
                Tempo passou e o danado do nome ainda hoje é mal dito por quem
                não dialoga com o diferente.
              </p>
            </ImageBanner>
            <ImageBanner
              colored
              wrapper="col-span-1"
              title={'"Um defeito de Cor"'}
              data="sala5/defeito_de_cor_2.jpg"
            >
              <p slot="text">
                "Um defeito de cor", Museu de Arte do Rio de Janeiro (2023).
              </p>
            </ImageBanner>
            <ImageBanner
              title={'"Um defeito de Cor"'}
              data="sala5/defeito_de_cor_1.jpg"
            >
              <p slot="text">
                "Um defeito de cor", Museu de Arte do Rio de Janeiro (2023).
              </p>
            </ImageBanner>

            <ImageBanner
              title={'"Um defeito de Cor"'}
              data="sala5/defeito_de_cor_4.jpg"
            >
              <p slot="text">
                "Um defeito de cor", Museu de Arte do Rio de Janeiro (2023).
              </p>
            </ImageBanner>
            <div />
            <ImageBanner
              title={'"Um defeito de Cor"'}
              data="sala5/defeito_de_cor_3.jpg"
            >
              <p slot="text">
                "Um defeito de cor", Museu de Arte do Rio de Janeiro (2023).
              </p>
            </ImageBanner>
          </div>

          <h2
            class="text-3xl tracking-wide font-quickbold py-10 mt-10 text-center"
          >
            Videos
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              title={"Documentário A dona do terreiro"}
              data={"https://www.youtube.com/embed/6wP1Tg8MF2I?si=5Z_tk1Dzqh4sC2dF&amp;clip=Ugkx5gHYTOH6Ed3t08vknNWOz-icOLa4_1Nz&amp;clipt=EJ_eBhi30wc"}
              thumbnail="sala5/a_dona_terreiro_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>
            <ImageBanner
              title={'Documentário IGI OBA NILE "Memórias de Mãe Raidalva"'}
              data={"https://www.youtube.com/embed/IAUx0PHMysw?si=YIbVWb3BkF8iXHZK&amp;clip=Ugkx-qr8yOI9IbQiJszMuT8lFsX2qg30VeF-&amp;clipt=EPXG8AEYjbzxAQ"}
              thumbnail="sala5/ig_oba_nile_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>

            <ImageBanner
              title={"Documentário A FLOR DO CANDOMBLÉ"}
              data={"https://www.youtube.com/embed/UmzuWFFJz2k?si=D89gU8s1djCLdWiw"}
              thumbnail="sala5/a_flor_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>

            <ImageBanner
              title={"Documentário de Umbanda - Maria do Espírito Santo - Preta Mandinga"}
              data={"https://www.youtube.com/embed/BrhM2XZx1nk?si=3bs7wqLVXMx4ZHwG&amp;clip=Ugkx2LWXZx5wNvt0xpW4zRxR_E2d7zTYea74&amp;clipt=EJvIAxjmgQU"}
              thumbnail="sala5/maria_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>

            <ImageBanner
              title={"Documentário Dona Luiza Yemanjá"}
              data={"https://www.youtube.com/embed/DgnZjoBgejY?si=vYMElNXEdoX44iMt"}
              thumbnail="sala5/luiza_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>

            <ImageBanner
              title={"Documentário Mãe Stella de Oxossi"}
              data={"https://www.youtube.com/embed/vSCeTpCGKQY?si=Gq-mrUJvqKH73UtF&amp;clip=UgkxFyl342q2A9_-4T9C1psFvYWdwmtszm1m&amp;clipt=ENrCARi5lwU"}
              thumbnail="sala5/mae_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>
            <div />
            <ImageBanner
              title={"Documentário Folhas Encantadas"}
              data={"https://www.youtube.com/embed/aT-Ng2Yw6QM?si=TAThm4a5yrXoIts0&amp;clip=UgkxdBQdWoxhRmP3zkif_TRMGWH6GMDLSSVU&amp;clipt=EKm2Kxjl5S4"}
              thumbnail="sala5/folhas_thumb.png"
            >
              <p slot="text"></p>
            </ImageBanner>
          </div>

          <h2
            class="text-3xl tracking-wide font-quickbold py-10 mt-10 text-center"
          >
            Casos
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              title="Jornal"
              data={[
                "sala5/lazaro_1.jpg",
                "sala5/lazaro_2.jpg",
                "sala5/lazaro_3.jpg",
              ]}
            >
              <p slot="text">
                Num tempo não tão distante, o caso do assassino Lázaro
                amedrontou criancinhas e adultos de todo o Brasil. Após matar
                uma família inteira e fugir da polícia por sete dias, o que
                tinha tudo para ser um filme de ação, com muita morte, sangue e
                fuga pelo caminho, ganhava as páginas online do portal G1 como
                um thriller de terror, com muita morte, sangue e preconceito.

                <br /><br />“Fotos mostram que casa de Lázaro Barbosa, suspeito
                de chacina em Ceilândia, tem itens que indicam bruxaria e
                rituais, diz polícia”.

                <br /><br />O título rapidamente ganhou as redes.
                Preconceituosamente sensacionalista, a manchete veiculada no
                portal G1, em 16 de junho de 2021, parecia replicar práticas que
                há mais de 100 anos se vestem de acesso à informação –
                lembrem-se do Quebra de Xangô de 1912 - quando, no fundo, no
                fundo (e na superfície mais que tudo) só espalham preconceito.

                <br /><br />Não demorou muito para que o público passasse a
                relacionar a foto divulgada na matéria (uma imagem aleatória de
                um assentamento de Exu que não tem nada a ver com bruxaria,
                criminalidade, Lázaro) com religiões de matrizes africanas.
                Ataques intolerantes e racistas ocuparam as redes. Após a
                repercussão, o portal desculpou-se “pelos erros no processo de
                publicação desta reportagem”, editando o texto e alterando o
                título para “Polícia divulga fotos da casa de Lázaro em Goiás”.

                <br /><br />Polícia divulga fotos da casa de Lázaro em Goiás |
                Goiás | G1 (globo.com) Caso Lázaro: G1 pede desculpas depois de
                críticas sobre intolerância religiosa (poder360.com.br)
              </p>
            </ImageBanner>
            <ImageBanner
              title="Falsa relação de religiões de matriz africana com bruxaria
          estampa a manchete do Jornal de Alagoas"
              data="sala5/jornal.jpg"
              colored="true"
            >
              <p slot="text">
                Falsa relação de religiões de matriz africana com bruxaria
                estampa a manchete do Jornal de Alagoas, 4 fev. 1912, quando 150
                xangôs foram destruídos naquele que entraria para a história
                como o maior ato de intolerância religiosa do Brasil. Fonte:
                Acervo do Instituto Histórico e Geográfico de Alagoas. <br />
                <br />“Xangô em acção — A oligarchia e o O povo invade os covis
                — Documentos preciosos — Um bode sacrificado — Exposição de
                ídolos e bugigangas” , acompanha o título da reportagem BRUXARIA
                na capa do Jornal de Alagoas de 4 de fevereiro de 1912.<br /><br
                /> A resistência da religiosidade de matriz africana em Alagoas -
                Jornalismo Júnior (jornalismojunior.com.br)
              </p>
            </ImageBanner>
            <ImageBanner
              title="Terreiro de candomblé é destruído em Duque de Caxias, na Baixada Fluminense"
              data="sala5/reportagem_6.jpg"
            >
              <p slot="text">
                Traficantes atacaram um terreiro de candomblé localizado no
                bairro Parque Paulista, em Duque de Caxias, na Baixada
                Fluminense. O crime ocorreu nesta quinta-feira (11).<br />
                Disponível em:<br />
                https://g1.globo.com/rj/rio-de-janeiro/noticia/2019/07/12/terreiro-de-candomble-e-destruido-em-duque-de-caxias-na-baixada-fluminense.ghtml
              </p>
            </ImageBanner>
            <ImageBanner
              title="Um Rio de ódio: terreiro de candomblé é atacado com pedras, ovos e legumes podres"
              data="sala5/reportagem_7.jpg"
            >
              <p slot="text">
                Os feixes de luz que, durante o dia, invadem o terreiro Ilê Axé
                Obá Inã, na Penha, Zona Norte do Rio, não têm nenhuma motivação
                decorativa ou espiritual. Os buracos nas telhas de alumínio, por
                onde os raios de sol invadem o local de culto, são reflexo do
                preconceito, manifestado na forma de pedras portuguesas lançadas
                recorrentemente sobre o espaço há pelo menos um ano e meio,
                perfurando o teto e a dignidade dos frequentadores — uma
                perseguição que não cessou nem com as denúncias à polícia. No
                terceiro dia da série de reportagens “Um Rio de ódio”, o EXTRA
                revela a marca da intolerância religiosa no estado, que em mais
                de um terço dos registros de ocorrência do gênero atinge
                seguidores da umbanda e do candomblé.<br />
                Disponível em:<br />
                https://extra.globo.com/casos-de-policia/um-rio-de-odio-terreiro-de-candomble-atacado-com-pedras-ovos-legumes-podres-21645654.html
              </p>
            </ImageBanner>
            <ImageBanner
              title="Ex-prefeito detalha “bruxaria” de adversária e é absolvido em ação"
              data="sala5/reportagem_8.jpg"
            >
              <p slot="text">
                A Justiça absolveu o ex-prefeito de Itaúba (580 km de Cuiabá),
                Raimundo Zanon (PSD), em uma ação penal por injúria movida pela
                sua adversária na campanha de 2012, Rosana Rebussi (PTB), em
                razão de tê-la acusado de fazer “bruxaria” contra ele..<br />
                Disponível em:<br />
                https://www.midianews.com.br/judiciario/ex-prefeito-detalha-bruxaria-de-adversaria-e-e-absolvido-em-acao/312141
              </p>
            </ImageBanner>
          </div>

          <h2
            class="text-3xl tracking-wide font-quickbold py-10 mt-10 text-center"
          >
            Extras
          </h2>
          <div class="w-full grid grid-cols-3 gap-4">
            <ImageBanner
              title="Cadastro dos espaços de matriz africanas será apresentado"
              data="sala5/reportagem_1.jpg"
            >
              <p slot="text">
                O cadastramento dos espaços de matriz africana e comunidades de
                terreiros da região metropolitana de João Pessoa, resultante de
                uma parceria entre a Casa de Cultura Ilê Asé D'Osoguiã e o
                Governo do Estado, por meio da Secretaria de Estado da Mulher e
                da Diversidade Humana (Semdh), será apresentado nesta
                terça-feira (21), às 8h, na sede da Ordem dos Advogados do
                Brasil (OAB-PB), em João Pessoa, pelo Instituto de Planejamento,
                Pesquisa, Comunicação, Estudos Sociais e Tecnológicos (IPPECET).

                <br /><br />Disponível em:
                https://paraiba.pb.gov.br/noticias/cadastro-dos-espacos-de-matriz-africana-sera-apresentado-nesta-terca-feira
              </p>
            </ImageBanner>
            <ImageBanner
              title="Pesquisa do Instituto Darcy Ribeiro identifica 300 templos religiosos em Maricá"
              data="sala5/reportagem_2.jpg"
            >
              <p slot="text">
                A Prefeitura de Maricá, por meio do Instituto Municipal de
                Informação e Pesquisa Darcy Ribeiro (IDR), apresentou nesta
                quarta-feira (20/09), no auditório da Câmara Municipal de
                Maricá, o resultado do Censo Matriz Africana e Terreiros, que
                identificou 300 templos religiosos no município. Deste total,
                235 pesquisas foram realizadas pela equipe, 44 estavam fechados
                permanentemente e 22 recusas ou ausentes. A parcial foi
                apresentada aos grupos que realizam práticas ritualísticas e
                ancestrais em todo o território de Maricá.

                <br /> <br />Disponível em:
                https://www.marica.rj.gov.br/noticia/pesquisa-do-instituto-darcy-ribeiro-identifica-300-templos-religiosos-em-marica/
              </p>
            </ImageBanner>
            <ImageBanner
              title="CADASTRAMENTO DOS TERREIROS MATRIZ-AFRICANA E AFRO-INDÍGENA"
              data="sala5/reportagem_3.jpg"
            >
              <p slot="text">
                O formulário de cadastramento de Comunidades Tradicionais de
                Terreiro (CTT) de Pernambuco está temporariamente suspenso pela
                Secretaria Executiva de Promoção da Equidade Social. O
                cadastramento irá retornar, em breve.
                <br /> <br />Disponível em:
                https://www.sdscjpvd.pe.gov.br/seses/formulario-de-cadastramento-das-organizacoes-religiosas/
              </p>
            </ImageBanner>
            <ImageBanner
              title="CTR - Cadastro de Templos Religiosos - Efetuar Adesão"
              data="sala5/reportagem_4.jpg"
            >
              <p slot="text">
                Efetuar adesão ao Cadastro de Templos Religiosos-CTR, o qual
                visa facilitar o reconhecimento do direito à isenção, imunidade
                ou não incidência tributária referente ao patrimônio, à renda e
                aos serviços relacionados com as atividades essenciais dos
                templos de qualquer culto.
                <br /> <br />Disponível em:
                https://mobile.receita.fazenda.df.gov.br/aplicacoes/CartaServicos/servico.cfm?codTipoPessoa=7&codServico=1127&codSubCategoria=132
              </p>
            </ImageBanner>
            <ImageBanner
              title="Prefeitura realiza Cadastro Único itinerante em comunidades de religiões de matrizes africanas"
              data="sala5/reportagem_5.jpg"
            >
              <p slot="text">
                Para fortalecer o processo de inclusão e garantia de direitos de
                todos os cidadãos aracajuanos, a Prefeitura de Aracaju, por meio
                da Assistência Social de Aracaju, iniciou uma série de mutirões
                itinerantes de cadastramento de pessoas de religiões de matrizes
                africanas.
                <br /> <br />Disponível em:
                https://www.aracaju.se.gov.br/noticias/84249/prefeitura_realiza_cadastro_unico_itinerante_em_comunidades_de_religioes_de_matrizes_africanas.html
              </p>
            </ImageBanner>

            <ImageBanner
              title="Os Intelectuais alagoanos e o Quebra de Xangô de 1912"
              data={"sala5/intelec_thumb.png"}
            >
              <p slot="text">
                Disponível em :<br />
                https://www.repositorio.ufal.br/bitstream/riufal/3756/1/Os%20Intelectuais%20alagoanos%20e%20o%20Quebra%20de%20Xang%C3%B4%20de%201912:%20uma%20hist%C3%B3ria%20de%20sil%C3%AAncios%20(1930-1950).pdf
              </p>
            </ImageBanner>
          </div>
          <div class="h-80"></div>
        </div>
      </div>
    </div>
  </div>
  <div class="h-80"></div>
</div>

<style>
  .teste {
    grid-column: span 2; /* Spans two columns for the last two items */
    text-align: center; /* Centers content horizontally */
  }
  .viewport {
    position: relative;
    overflow: scroll;
    border: 1px solid gray;
    box-sizing: border-box;

    /* hide scrollbar */
    -ms-overflow-style: none;
    scrollbar-width: none;
  }

  .viewport::-webkit-scrollbar {
    /* hide scrollbar */
    display: none;
  }
</style>
