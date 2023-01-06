<template>
  <section id="contact" class="contact">
    <h2
      id="section2"
      class="text-4xl text-center text-green-500/60 font-normal font-montserrat mb-8 tracking-wide drop-shadow-text-sm"
    >
      Contatos
    </h2>
    <div
      class="container justify-between text-center grid md:grid-cols-3 grid-cols-1 gap-4"
    >
      <div class="text-center">PORTO ALEGRE - RS BRASIL</div>
      <div class="text-center">
        CONTATO@<br />PARADISEENTRETENIMENTO.<br />COM.BR
      </div>
      <div class="text-center">FONE +55 (51) 99101 2803</div>
    </div>
    <div class="sm:text-center"></div>
    <div class="container">
      <div class="-mx-4 flex justify-center">
        <div class="px-4 w-10/12 sm:w-8/12">
          <div class="relative rounded-lg py-8 sm:py-12">
            <!-- Form Contact -->
            <form class="mb-16">
              <div class="mb-6">
                <input
                  type="text"
                  placeholder="Nome"
                  class="text-body-color border-gray-300 focus:border-primary w-full rounded border py-2 px-[14px] text-base outline-none focus-visible:shadow-none"
                />
              </div>
              <div class="mb-6">
                <input
                  type="email"
                  placeholder="Email"
                  class="text-body-color border-gray-300 focus:border-primary w-full rounded border py-2 px-[14px] text-base outline-none focus-visible:shadow-none"
                />
              </div>
              <div class="mb-6">
                <textarea
                  rows="6"
                  placeholder="Mesnagem"
                  class="text-body-color border-gray-300 focus:border-primary w-full resize-none rounded border py-2 px-[14px] text-base outline-none focus-visible:shadow-none"
                ></textarea>
              </div>
              <div>
                <button
                  type="submit"
                  class="bg-green-600 w-full rounded p-3 text-white transition hover:bg-opacity-90"
                >
                  Send Message
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped></style>
