<script setup lang="ts">
const navItems = [
  { label: 'Главная', id: 'hero' },
  { label: 'Платформа', id: 'platform' },
  { label: 'Mini Apps', id: 'apps' },
  { label: 'Token', id: 'token' },
  { label: 'Roadmap', id: 'roadmap' },
  { label: 'Контакты', id: 'contact' },
]
</script>

<template>
  <main class="text-white bg-#06142f min-h-screen overflow-x-hidden">
    <!-- Background -->
    <div class="pointer-events-none inset-0 fixed">
      <div class="rounded-full bg-cyan-400/20 h-80 w-80 left-[-25%] top-[-10%] absolute blur-3xl md:left-[-10%]" />
      <div class="rounded-full bg-blue-500/20 h-96 w-96 right-[-25%] top-40 absolute blur-3xl md:right-[-10%]" />
      <div class="bg-[linear-gradient(rgba(255,255,255,.06)_1px,transparent_1px),linear-gradient(90deg,rgba(255,255,255,.06)_1px,transparent_1px)] opacity-15 inset-0 absolute bg-size-[64px_64px]" />
    </div>

    <!-- Navbar -->
    <header class="px-3 py-3 left-0 right-0 top-0 fixed z-50 md:px-4 md:py-4">
      <div class="mx-auto px-4 py-3 border border-white/15 rounded-full bg-#06142f/75 flex max-w-1180px shadow-xl items-center justify-between backdrop-blur-xl md:px-5">
        <a href="#hero" class="flex gap-3 items-center">
          <div class="text-#06142f rounded-full bg-cyan-300 flex shrink-0 h-10 w-10 items-center justify-center">
            <div class="i-carbon-taxi text-xl" />
          </div>

          <div class="text-left">
            <p class="text-sm leading-4 font-900 md:text-base">
              Telegram Taxi
            </p>
            <p class="text-xs text-white/50">
              Mobility OS
            </p>
          </div>
        </a>

        <nav class="gap-1 hidden items-center lg:flex">
          <a
            v-for="item in navItems"
            :key="item.id"
            :href="`#${item.id}`"
            class="text-sm text-white/70 px-4 py-2 rounded-full transition hover:text-white hover:bg-white/10"
          >
            {{ item.label }}
          </a>
        </nav>

        <a
          href="#contact"
          class="text-sm text-#06142f font-900 px-4 py-2 rounded-full bg-cyan-300 shadow-cyan-400/20 shadow-lg transition md:px-5 hover:bg-cyan-200"
        >
          Связаться
        </a>
      </div>
    </header>

    <!-- Hero -->
    <section id="hero" class="px-5 pb-16 pt-30 flex min-h-screen items-center relative scroll-mt-28 md:pt-36">
      <div class="mx-auto gap-12 grid max-w-1180px items-center lg:grid-cols-2">
        <div>
          <div class="text-xs text-cyan-100 mb-6 px-4 py-2 border border-cyan-300/30 rounded-full bg-cyan-300/10 inline-flex gap-2 items-center md:text-sm">
            <div class="i-carbon-network-4" />
            Digital mobility ecosystem
          </div>

          <h1 class="text-5xl leading-none font-950 max-w-650px md:text-7xl">
            Telegram Taxi
          </h1>

          <p class="text-base text-white/70 leading-7 mt-6 max-w-560px md:text-lg md:leading-8">
            Инновационная экосистема для пассажиров, водителей и таксопарков.
            Заказ поездок, управление водителями и развитие сервиса прямо внутри Telegram Mini Apps.
          </p>

          <div class="mt-8 flex flex-col gap-3 sm:flex-row">
            <a
              href="#platform"
              class="text-#06142f font-900 px-7 py-4 rounded-full bg-cyan-300 inline-flex shadow-cyan-400/25 shadow-xl transition justify-center hover:bg-cyan-200"
            >
              Узнать больше →
            </a>

            <a
              href="#token"
              class="text-white font-800 px-7 py-4 border border-white/20 rounded-full bg-white/8 inline-flex transition justify-center backdrop-blur hover:bg-white/12"
            >
              Смотреть токен
            </a>
          </div>
        </div>

        <!-- Right card -->
        <div class="relative">
          <div class="rounded-50px bg-cyan-300/20 inset-0 absolute blur-3xl" />

          <div class="p-3 border border-cyan-200/25 rounded-36px bg-white/10 shadow-2xl relative backdrop-blur-xl md:p-5 md:rounded-42px">
            <div class="p-5 border border-white/10 rounded-30px bg-#0a2148 md:p-7 md:rounded-34px">
              <div class="mb-6 flex gap-4 items-center justify-between">
                <div>
                  <p class="text-sm text-white/50">
                    Telegram Taxi network
                  </p>
                  <h2 class="text-2xl font-900">
                    Mobility OS
                  </h2>
                </div>

                <div class="text-#06142f rounded-2xl bg-cyan-300 flex shrink-0 h-12 w-12 items-center justify-center md:h-13 md:w-13">
                  <div class="i-carbon-bus text-2xl" />
                </div>
              </div>

              <div class="border border-white/10 rounded-3xl bg-#102b5c h-230px relative overflow-hidden md:h-260px">
                <div class="border border-cyan-300/80 rounded-full bg-cyan-300/10 h-24 w-24 left-8 top-8 absolute" />
                <div class="border border-cyan-300/70 rounded-full bg-cyan-300/10 h-22 w-22 right-8 top-18 absolute" />
                <div class="border border-cyan-300/70 rounded-full bg-cyan-300/10 h-28 w-28 bottom-8 right-14 absolute" />

                <div class="bg-cyan-300/60 h-1 w-48 left-18 top-34 absolute md:w-58 md:left-22" />

                <div class="px-4 py-3 border border-white/15 rounded-2xl bg-white/15 left-5 top-30 absolute backdrop-blur md:left-9">
                  <p class="text-xs text-white/60">
                    Passengers
                  </p>
                  <p class="font-900">
                    Connected
                  </p>
                </div>

                <div class="px-4 py-3 border border-white/15 rounded-2xl bg-white/15 right-5 top-16 absolute backdrop-blur md:right-8">
                  <p class="text-xs text-white/60">
                    Drivers
                  </p>
                  <p class="font-900">
                    Online
                  </p>
                </div>

                <div class="text-cyan-500 rounded-full bg-white flex h-18 w-18 shadow-xl items-center left-1/2 top-1/2 justify-center absolute md:h-20 md:w-20 -translate-x-1/2 -translate-y-1/2">
                  <div class="i-carbon-send-alt-filled text-3xl" />
                </div>
              </div>

              <div class="mt-5 gap-3 grid grid-cols-2 md:gap-4">
                <div class="p-4 border border-white/10 rounded-2xl bg-white/8">
                  <p class="text-xs text-white/50">
                    Market
                  </p>
                  <p class="text-lg font-900">
                    Kazakhstan
                  </p>
                </div>

                <div class="p-4 border border-white/10 rounded-2xl bg-white/8">
                  <p class="text-xs text-white/50">
                    Token
                  </p>
                  <p class="text-lg font-900">
                    TAXI
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Platform -->
    <section id="platform" class="px-5 py-20 relative scroll-mt-28 md:py-28">
      <div class="mx-auto max-w-1180px">
        <div class="p-6 border border-white/10 rounded-4xl bg-white/6 backdrop-blur md:p-10">
          <p class="text-sm text-cyan-300 font-800">
            Platform
          </p>

          <h2 class="text-3xl font-900 mt-3 md:text-4xl">
            Платформа
          </h2>

          <p class="text-white/60 leading-8 mt-4 max-w-760px">
            Telegram Taxi объединяет пассажирское приложение, приложение водителя,
            систему заказов, рейтинги, оплату, аналитику и будущую токен-экономику.
          </p>
        </div>
      </div>
    </section>

    <!-- Apps -->
    <section id="apps" class="px-5 py-20 relative scroll-mt-28 md:py-28">
      <div class="mx-auto max-w-1180px">
        <div class="mb-8">
          <p class="text-sm text-cyan-300 font-800">
            Mini Apps
          </p>
          <h2 class="text-3xl font-900 mt-3 md:text-4xl">
            Два приложения внутри Telegram
          </h2>
        </div>

        <div class="gap-5 grid md:grid-cols-2">
          <div class="p-7 border border-white/10 rounded-4xl bg-white/8 transition backdrop-blur md:p-8 hover:border-cyan-300/30">
            <div class="rounded-2xl bg-cyan-300/10 flex h-14 w-14 items-center justify-center">
              <div class="i-carbon-user-avatar text-4xl text-cyan-300" />
            </div>

            <h3 class="text-2xl font-900 mt-6">
              Passenger Mini App
            </h3>

            <p class="text-white/60 leading-7 mt-4">
              Заказ поездки, выбор адресов, тарифы, история поездок и отслеживание водителя.
            </p>
          </div>

          <div class="p-7 border border-white/10 rounded-4xl bg-white/8 transition backdrop-blur md:p-8 hover:border-cyan-300/30">
            <div class="rounded-2xl bg-cyan-300/10 flex h-14 w-14 items-center justify-center">
              <div class="i-carbon-car text-4xl text-cyan-300" />
            </div>

            <h3 class="text-2xl font-900 mt-6">
              Driver Mini App
            </h3>

            <p class="text-white/60 leading-7 mt-4">
              Онлайн-статус, принятие заказов, профиль, автомобиль и управление поездками.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Token -->
    <section id="token" class="px-5 py-20 relative scroll-mt-28 md:py-28">
      <div class="mx-auto p-7 border border-cyan-300/20 rounded-4xl bg-cyan-300/8 max-w-1180px backdrop-blur md:p-10">
        <p class="text-cyan-300 font-800">
          Ecosystem Token
        </p>

        <h2 class="text-3xl font-900 mt-3 md:text-4xl">
          TAXI Token
        </h2>

        <p class="text-white/60 leading-8 mt-4 max-w-760px">
          Utility token для бонусов водителям, программ лояльности пассажиров,
          реферальных наград, скидок, промо-кампаний и будущих функций экосистемы.
        </p>
      </div>
    </section>

    <!-- Roadmap -->
    <section id="roadmap" class="px-5 py-20 relative scroll-mt-28 md:py-28">
      <div class="mx-auto max-w-1180px">
        <p class="text-sm text-cyan-300 font-800">
          Roadmap
        </p>

        <h2 class="text-3xl font-900 mt-3 md:text-4xl">
          План развития
        </h2>

        <div class="mt-8 gap-4 grid lg:grid-cols-4 sm:grid-cols-2">
          <div class="p-6 border border-white/10 rounded-3xl bg-white/8 backdrop-blur">
            <p class="text-sm text-cyan-300">
              Phase 1
            </p>
            <b class="text-xl mt-2 block">Development</b>
          </div>

          <div class="p-6 border border-white/10 rounded-3xl bg-white/8 backdrop-blur">
            <p class="text-sm text-cyan-300">
              Phase 2
            </p>
            <b class="text-xl mt-2 block">Kazakhstan Launch</b>
          </div>

          <div class="p-6 border border-white/10 rounded-3xl bg-white/8 backdrop-blur">
            <p class="text-sm text-cyan-300">
              Phase 3
            </p>
            <b class="text-xl mt-2 block">Central Asia</b>
          </div>

          <div class="p-6 border border-white/10 rounded-3xl bg-white/8 backdrop-blur">
            <p class="text-sm text-cyan-300">
              Phase 4
            </p>
            <b class="text-xl mt-2 block">International</b>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="px-5 pb-10 pt-20 relative scroll-mt-28 md:pb-16 md:pt-28">
      <div class="text-#06142f mx-auto p-7 rounded-4xl bg-cyan-300 max-w-1180px overflow-hidden md:p-10">
        <div class="gap-6 grid md:grid-cols-[1fr_auto] md:items-center">
          <div>
            <h2 class="text-3xl leading-tight font-950 md:text-4xl">
              Ride smarter through Telegram
            </h2>

            <p class="leading-7 font-600 mt-4">
              Website: telegramtaxi.kz · Email: info@telegramtaxi.kz
            </p>
          </div>

          <a
            href="mailto:info@telegramtaxi.kz"
            class="text-white font-900 px-7 py-4 rounded-full bg-#06142f inline-flex transition justify-center hover:bg-#0a2148"
          >
            Написать
          </a>
        </div>
      </div>
    </section>
  </main>
</template>
