<script>
  import { faker } from "@faker-js/faker";
  const helpers = faker.helpers.contextualCard();
  console.log(helpers);

  let person = {
    name: helpers.name,
    username: helpers.username,
    city: helpers.address.city,
    phone: helpers.phone,
    companyName: helpers.company.name,
    avatar: helpers.avatar,
  };
  export let id;
 

</script>

<div class="a-table-row" class:colorTwo={id%2===0}>
  <div class="col col-id">{id}</div>
  <div class="col col-name">{person.name}</div>
  <div class="col col-username">{person.username}</div>
  <div class="col col-city">{person.city}</div>
  <div class="col col-company">{person.companyName}</div>
  <div class="col col-phone">{person.phone}</div>
  <img src={person.avatar} alt="{person.username} avatar" />
</div>

<style>
  .a-table-row {
    display: table;
    width: 90%;
    margin-left: 3.5%;
    background-color: #a4e07f;
   
  }

  .col {
    display: inline-table;
    width: 15%;
  }
  .colorTwo{
    background-color: #ebffba;
  }
</style>
