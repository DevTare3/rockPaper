<script lang="ts">
  import * as AlertDialog from "$lib/components/ui/alert-dialog/index.js";
  import bg from "$lib/images/bg-pentagon.svg";
</script>

<AlertDialog.Root>
  <AlertDialog.Trigger>RULES</AlertDialog.Trigger>
  <AlertDialog.Content>
    <AlertDialog.Header>
      <AlertDialog.Title>RULES</AlertDialog.Title>
      <AlertDialog.Description>
        <img src={bg} alt="Rules of the game" />
      </AlertDialog.Description>
    </AlertDialog.Header>
    <AlertDialog.Footer>
      <AlertDialog.Cancel></AlertDialog.Cancel>
    </AlertDialog.Footer>
  </AlertDialog.Content>
</AlertDialog.Root>
