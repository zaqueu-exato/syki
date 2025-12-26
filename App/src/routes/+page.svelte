<script lang="ts">
    let { data } = $props();
    import * as Accordion from "$lib/components/ui/accordion/index.js";
  import * as AlertDialog from "$lib/components/ui/alert-dialog/index.js";
  import { buttonVariants } from "$lib/components/ui/button/index.js";
</script>

<h1>---</h1>

<h1>Welcome to ESTUD!</h1>

<Accordion.Root type="single" class="w-full sm:max-w-[70%]" value="item-1">
  <Accordion.Item value="item-1">
    <Accordion.Trigger>Product Information</Accordion.Trigger>
    <Accordion.Content class="flex flex-col gap-4 text-balance">
      <p>
        Our flagship product combines cutting-edge technology with sleek design.
        Built with premium materials, it offers unparalleled performance and
        reliability.
      </p>
      <p>
        Key features include advanced processing capabilities, and an intuitive
        user interface designed for both beginners and experts.
      </p>
    </Accordion.Content>
  </Accordion.Item>
  <Accordion.Item value="item-2">
    <Accordion.Trigger>Shipping Details</Accordion.Trigger>
    <Accordion.Content class="flex flex-col gap-4 text-balance">
      <p>
        We offer worldwide shipping through trusted courier partners. Standard
        delivery takes 3-5 business days, while express shipping ensures
        delivery within 1-2 business days.
      </p>
      <p>
        All orders are carefully packaged and fully insured. Track your shipment
        in real-time through our dedicated tracking portal.
      </p>
    </Accordion.Content>
  </Accordion.Item>
  <Accordion.Item value="item-3">
    <Accordion.Trigger>Return Policy</Accordion.Trigger>
    <Accordion.Content class="flex flex-col gap-4 text-balance">
      <p>
        We stand behind our products with a comprehensive 30-day return policy.
        If you&apos;re not completely satisfied, simply return the item in its
        original condition.
      </p>
      <p>
        Our hassle-free return process includes free return shipping and full
        refunds processed within 48 hours of receiving the returned item.
      </p>
    </Accordion.Content>
  </Accordion.Item>
</Accordion.Root>


<AlertDialog.Root>
  <AlertDialog.Trigger class={buttonVariants({ variant: "outline" })}>
    Show Dialog Now
  </AlertDialog.Trigger>
  <AlertDialog.Content>
    <AlertDialog.Header>
      <AlertDialog.Title>Are you absolutely sure?</AlertDialog.Title>
      <AlertDialog.Description>
        This action cannot be undone. This will permanently delete your account and remove your data from our servers. Ok?
      </AlertDialog.Description>
    </AlertDialog.Header>
    <AlertDialog.Footer>
      <AlertDialog.Cancel>Cancel</AlertDialog.Cancel>
      <AlertDialog.Action>Continue</AlertDialog.Action>
    </AlertDialog.Footer>
  </AlertDialog.Content>
</AlertDialog.Root>
