<script>
  import SectionTitle from "./SectionTitle.svelte";
</script>

<SectionTitle title="Contact"/>
<div class="content">
  <form name="contact" method="post">
    <div>
      <label for="name">Name</label><br />
      <input type="text" id="name" name="name" value="" />
    </div>
    <div>
      <label for="email">Email</label><br />
      <input type="email" id="email" name="email" value="" />
    </div>
    <div>
      <label for="Phone">Phone</label><br />
      <input type="tel" id="Phone" name="Phone" value="" />
    </div>
    <div>
      <label for="Message">Message</label><br />
      <textarea id="Phone" name="Message" value="" />
    </div>
    <input type="hidden" name="form-name" value="contact" />
    <input type="submit" value="Submit">
  </form>
</div>

<style>
  form {
    text-align: left;
    margin: auto;
    width: 35%;
    padding-top: 20px;
    color: white;
    text-transform: uppercase;
  }
  input:focus,
  textarea:focus{
    outline: none;
  }
  input, textarea {
    width: 100%;
    background-color: transparent;
    border: none;
    border-bottom: 2px solid white;
    margin-bottom: 10px;
    padding: 10px;
    color: white;
  }
  label {
    background-color: #171717;
    line-height: 23px;
    font-size: 25px;
  }

  input[type="submit"] {
    border: none;
    text-transform: uppercase;
    background-color: #171717;
    font-size: 30px;
  }

  @media only screen and (max-width: 1500px) {
    form {
    width: 50%;
    }
  }
  @media only screen and (max-width: 1200px) {
    form {
    width: 60%;
    }
  }

  @media only screen and (max-width: 980px) {
    form {
    width: 80%;
    }
  }
</style>
