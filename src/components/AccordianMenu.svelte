<script>
  import AccordianSection from "./AccordianSection.svelte";
  const cfpItems = [{ target: "/gc-2021/cfp", label: "Call for Proposals" }];
  const agendaItems = [
    { target: "/gc-2021/agenda", label: "Call for Proposals" },
  ];
  const speakersItems = [
    { target: "/gc-2021/speakers", label: "Call for Proposals" },
  ];
  const sponsorsItems = [
    { target: "/gc-2021/sponsors", label: "Call for Proposals" },
  ];
  const venueItems = [
    { target: "/gc-2021/venue", label: "Call for Proposals" },
  ];
</script>

<div class="accordion-container">
  <AccordianSection title="CFP" section="cfp" items={cfpItems} />
  <AccordianSection title="Speakers" section="speakers" items={speakersItems} />
  <AccordianSection title="Sponsors" section="sponsors" items={sponsorsItems} />
  <AccordianSection title="Agenda" section="agenda" items={agendaItems} />
  <AccordianSection title="Venue" section="venue" items={venueItems} />
</div>
