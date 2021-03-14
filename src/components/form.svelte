<form on:submit|preventDefault>
  <input placeholder="Name..." type="text" />
  <input placeholder="Email..." type="text" />
  <textarea placeholder="Message..." />
  <button>Submit</button>
</form>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  form {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  input,
  textarea,
  button {
    margin: 1em 0;
    padding: 1em;
  }
  button {
    background: #f60;
    color: azure;
    font-weight: bold;
    border: none;
    outline: none;
  }
</style>
