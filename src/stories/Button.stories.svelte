<script>
  import { Meta, Template, Story } from "@storybook/addon-svelte-csf";
  import Button from "../lib/Button.svelte";
</script>

<Meta
  title="Button"
  component={Button}
  argTypes={{
    label: { control: "text" },
    primary: { control: "boolean" },
    size: {
      control: { type: "select", options: ["small", "medium", "large"] },
    },
    onClick: { action: "onClick" },
  }}
/>


<Template let:args>
  <Button {...args} on:click={args.onClick} />
</Template>


<Story
  name="Primary"
  args={{
    primary: true,
    label: "Button",
  }}
/>

<Story
  name="Secondary"
  args={{
    primary: false,
    label: "Button",
  }}
/>

<Story
  name="Large"
  args={{
    size: "large",
    label: "Button",
  }}
/>

<Story
  name="Medium"
  args={{
    size: "medium",
    label: "Button",
  }}
/>

<Story
  name="Small"
  args={{
    size: "small",
    label: "Button",
  }}
/>
