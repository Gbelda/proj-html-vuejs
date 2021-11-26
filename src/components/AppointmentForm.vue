<template>
  <div class="form d-flex justify-between flex-wrap">
    <input type="text" class="w50" placeholder="Name*" required />
    <input type="email" class="w50" placeholder="Email*" required />
    <input type="text" class="w50" placeholder="Phone Number" />
    <div class="w50 date d-flex">
      <div class="calendar_img">
        <img src="../assets/img/calendar.svg" alt="" class="calendar" />
      </div>
      <input
        type="text"
        name="appointment"
        placeholder="Appointment Date"
        onfocus="(this.type='date')"
        onblur="(this.type='text')"
        class="date_input"
      />
    </div>
    <textarea
      name="query"
      id="query"
      cols="90"
      rows="10"
      placeholder="How can we help?*"
      required
    ></textarea>
    <button class="submit">MAKE AN APPOINTMENT</button>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";
.form {
  width: 35%;
  margin: auto;

  .w50 {
    width: 49%;
  }

  input {
    margin-bottom: 2rem;
    height: 40px;
    text-indent: 1rem;
    position: relative;
    background-color: transparent;
    border: 1px solid rgb(194, 194, 194);
    color: white;

    &::placeholder {
      color: rgb(194, 194, 194);
    }
  }

  .date {
    max-height: 40px;
    .date_input {
      width: 100%;
      text-indent: 2rem;
    }

    .calendar_img {
      padding-left: 15px;
      margin-right: -25px;
      padding-top: 6px;

      .calendar {
        width: 10px;
        filter: invert(0.6);
        padding-left: 1px;
      }
    }

    input::-webkit-datetime-edit {
      position: relative;
      left: 15px;
    }

    input::-webkit-datetime-edit-fields-wrapper {
      position: relative;
      left: 15px;
    }
  }

  textarea {
    padding-left: 1rem;
    padding-top: 1rem;
    background-color: transparent;
    font-family: "Noto Sans JP", sans-serif;
    border: 1px solid rgb(194, 194, 194);
    margin-bottom: 2rem;
    color: white;

    &::placeholder {
      color: rgb(194, 194, 194);
    }
  }

  button {
    width: 100%;
    height: 60px;
    font-size: 1.5rem;
    color: white;
    background-color: $highlight_primary;
    border: none;
    margin-bottom: 10rem;
  }
}
</style>