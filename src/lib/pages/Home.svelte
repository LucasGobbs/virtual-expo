<script>
  import Section from '../components/Section.svelte';
  import { link } from "svelte-spa-router";
  import { onMount } from 'svelte';
  import AOS from 'aos'
  onMount(() => {
		AOS.init()
	})
  const lorem = "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum."
  
  
  const sections = [
    {
      title: 'Bruxaria',
      icon: {},
      text: [
        `Na Idade Média, as mulheres que tinham comportamentos que fugiam dos padrões da época eram consideradas criminosas, perversas, ignorantes e supersticiosas, logo, feiticeiras. Ligadas a crenças pagãs arraigadas, especialmente nas áreas rurais, essas mulheres, devido à sua condição social frágil e falta de conhecimento, eram mais propensas a se envolver em práticas supersticiosas e ilusões atribuídas ao Diabo.
        
        
        
        
        
        
        
        
        `],
      url: 'sala2',
      image: 'a_bruxa_albrecht_durer.png',
      tint: 'rgb(158, 157, 157)',
      filter: 'grayscale(100%)'
    },
    {
      title: 'Bruxaria no Brasil',
      icon: {},
      text: [
        `As autoridades portuguesas consideravam a colônia como lar de hereges, feiticeiros e outros colonos que desafiavam a ordem estabelecida. O temor em relação às forças malignas crescia constantemente, especialmente a partir do século XIII, quando desastres naturais, pestes e fome geravam um pavor no homem, atribuindo ao diabo a origem de todas as calamidades, uma após a outra. A invenção da imprensa contribuiu para essa disseminação.`,
        `"Cristãos-Novos, sodomitas, hereges calvinistas, feiticeiros, magos, adivinhos só podiam ser entendidos no contexto em que viviam: o Universo colonial com toda sua complexidade, o cotidiano dos colonos com suas aspirações diversas, às vezes nobres e legítimas, outras vezes medíocres e mesquinhas" (SOUZA, 1986, p.153).`
      ],
      image: 'calundu.png',
      tint: 'rgb(58, 86, 54)'
    },
    {
      title: 'Visitas Pastorais e Visitações do Santo Ofício no Brasil Colonial',
      icon: {},
      text: [
        `A presença do Tribunal do Santo Ofício no Brasil foi representada pelas autoridades eclesiásticas locais, que tinham a autonomia para identificar casos de desobediência à fé, conduzir investigações preliminares e prender suspeitos, encaminhando-os para Lisboa, onde o processo era finalizado. Essa estrutura operou entre os séculos XVI e XVIII. Embora a sede estivesse distante, a Inquisição demonstrou sua influência de forma muito próxima, especialmente quando enviava funcionários para visitas a áreas cruciais da Colônia.`,
        `Essas visitas eram eventos de grande importância. A chegada do emissário mobilizava a população e gerava procissões. Acompanhado por um séquito numeroso, o visitador era recebido em uma residência central, onde o governador-geral, autoridades de alto escalão, juízes, bispos, vigários e missionários se apresentavam em sinal de respeito.`
      ],
      image: 'ilustracao_kleber_sales_1.png',
      tint: ''
    },
    {
      title: '',
      icon: {},
      text: [''],
      image: 'ilustracao_kleber_sales_2.png',
      tint: ''
    },
    {
      title: '',
      icon: {},
      text: [''],
      image: 'tela_debret.png',
      tint: ''
    },
    {
      title: '',
      icon: {},
      text: [''],
      image: 'tela_rugendas.png',
      tint: ''
    },
  ]

  
</script>

<svelte:head>
	<link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />
</svelte:head>

<div class="h-screen w-screen">
  <div class="text-white">
    <div class="bg-yellow-600 py-28 px-5 h-screen-80">
      <h2 class="transition delay-50  
        text-3xl tracking-wide font-quickbold">
        Mulheres e intolerância religiosa na Idade Moderna 
      </h2>

      <h3 class="transition delay-50  
        text-13xl tracking-wide font-quickbold py-5">
        Exposição Virtual | UFF
      </h3>
      <p>
        Exposição sobre tasdoaskd saokdoask doask odsak odask odk
        asdokasodkasokdkasokdasokdk oaskdokasok oaksdo kaos dokaso d
        asdkasokdoaskd asaodkasok asokdoas kosako dkasokd oaskod 
      </p>
    </div>
    
    {#each sections as section}
      <Section 
        title={section.title} 
        text={section.text} 
        tint={section.tint} 
        image={`./images/${section.image}`} 
        filter={section.filter}
        url={section.url}
      />
    {/each}
  </div>
</div>

<style>
  .h-screen-80 {
    height: 80vh;
  }

  .picker {
    background-color: rgb(118, 47, 165);
  }
</style>
