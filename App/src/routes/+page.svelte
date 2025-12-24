<script lang="ts">
  import { Accordion } from "bits-ui";
</script>

<h1>Welcome to ESTUD!</h1>

<Accordion.Root type="single">
  <Accordion.Item value="item-1">
    <Accordion.Header>
      <Accordion.Trigger>Students</Accordion.Trigger>
    </Accordion.Header>
    <Accordion.Content
      >This is the collapsible content for this section.</Accordion.Content
    >
  </Accordion.Item>
  <Accordion.Item value="item-2">
    <Accordion.Header>
      <Accordion.Trigger>Teachers</Accordion.Trigger>
    </Accordion.Header>
    <Accordion.Content
      >This is the collapsible content for this section.</Accordion.Content
    >
  </Accordion.Item>
</Accordion.Root>
