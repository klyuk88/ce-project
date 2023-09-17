<script setup>
import { TheButton } from "~/components/shared/ui/Button/";
import { ServiceItem } from "~/components/shared/ui/ServiceItem/";
import { ModalOverlay } from "~/components/shared/ui/Modal";
import { TheInput } from "~/components/shared/ui/Forms/Input";

const isShowModal = ref(false);
</script>
<template>
  <main>
    <section id="main" class="pt-11">
      <div class="ce-container">
        <h1
          class="text-[130px] uppercase font-semibold leading-[120px] flex flex-col items-start"
        >
          <span>Код <span class="text-accent">&lt;/&gt;</span> </span>
          <span>Экспресс</span>
        </h1>
        <div class="grid grid-cols-2 items-center mt-14">
          <div>
            <h2 class="text-2xl font-medium uppercase">
              Аутсорс веб-разработка
            </h2>
            <p class="mt-4 text-[18px]">
              Верстаем и программируем сайты, сервисы, интернет-магазины.
              Возьмем на себя часть или все работы по проекту, сократим время и
              затраты на разработку.
            </p>
          </div>
          <TheButton
            :btn-class="'w-[330px] ml-auto'"
            @click="isShowModal = true"
          >
            <template #title>Консультация</template>
          </TheButton>
        </div>
      </div>
    </section>

    <section id="about" class="sec-padding">
      <div class="ce-container">
        <div class="grid grid-cols-2">
          <div>
            <div
              class="rounded-br-[150px] w-[370px] h-[370px] bg-neutral-300 relative overflow-hidden z-10"
            >
              <div
                class="bg-accent absolute top-0 left-0 w-full h-1 z-20"
              ></div>
              <img
                src="@/assets/img/team.jpg"
                alt="team"
                class="absolute w-full h-full left-0 top-0 object-cover z-10"
              />
            </div>
          </div>
          <div>
            <h2 class="sec-title mt-4">О нас</h2>
            <p>
              Мы - аутсорсинговая IT компания, предоставляем услуги по
              веб-разработке на основе договора аутсорсинга. Сфокусированы на
              разработке веб-сайтов и веб-приложений. Возьмем на себя задачи,
              связанные с разработкой или поддержкой проекта.
              <br /><br />
              Наша миссия - создавать веб-сайты или приложения, которые будут
              соответствовать всем требованиям заказчика и приносить
              максимальную пользу пользователям.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="services" class="sec-padding">
      <div class="ce-container">
        <h2 class="sec-title">Услуги</h2>
        <div class="mt-10 flex flex-col gap-9">
          <ServiceItem title="Frontend разработка" price="1700">
            <template #description>
              <p>
                Разработаем удобный интерфейс для пользователей, который будет
                выглядеть хорошо на любом устройстве и в любом браузере.
                Запрограммируем логику приложения в соответсвии с тех заданием.
                Протестируем код, прежде чем выпускать в прод.
              </p>
            </template>
            <template #technologies>
              <p>
                HTML, CSS, JavaScript, SCSS, Figma, Gulp, Webpack, Vite, GSAP,
                Vue JS, NuxtJS, Node JS, TypeScript, Three JS, Jest, StoryBook
              </p>
            </template>
          </ServiceItem>

          <ServiceItem title="FullStack разработка" price="2200">
            <template #description>
              <p>
                Возьмем на себя все этапы разработки проекта.<br />–
                Проектирование архитектуры приложения; <br />– Создание базы
                данных;<br />
                – Разработка серверной части (back-end);<br />
                – Разработка клиентской части (front-end);<br />
                – Тестирование и отладка;<br />
                – Поддержка и обновление приложения;<br />
                Такой подход позволяет сократить время на разработку и повысить
                качество продукта.
              </p>
            </template>
            <template #technologies>
              <p>Frontend технологии + Strapi, SQLite, Postgress</p>
            </template>
          </ServiceItem>
          <ServiceItem title="Fronted разработка + CMS" price="2200">
            <template #description>
              <p>
                CMS позволяет администраторам и пользователям сайта легко
                создавать, редактировать и управлять контентом на сайте без
                необходимости знания программирования. CMS также может
                предоставлять дополнительные функции, такие как управление
                пользователями, безопасность, SEO, аналитика и т. д.
              </p>
            </template>
            <template #technologies>
              <p>Frontend технологии + Strapi, Word Press, Node JS, PHP</p>
            </template>
          </ServiceItem>
        </div>
      </div>
    </section>

    <section id="projects" class="sec-padding pb-[130px]">
      <div class="ce-container">
        <h2 class="sec-title leading-none">Проекты</h2>
        <p class="mt-4">
          Мы работаем с клиентами из разных отраслей и регионов, и всегда готовы
          предложить индивидуальный подход к каждому проекту. Занимаемся
          разработкой: от простых корпоративных сайтов до сложных
          интернет-магазинов и порталов, разработкой и внедренией CRM-систем,
          интеграцией веб-проектов с другими системами, такими как ERP,
          платежные системы и т. д.
        </p>

        <div class="grid grid-cols-2 gap-14 mt-10">
          <div>
            <div
              class="rounded-[25px] bg-neutral-200 w-full aspect-square cursor-pointer"
            ></div>
          </div>
          <div>
            <div
              class="rounded-[25px] bg-neutral-200 w-full aspect-square cursor-pointer"
            ></div>
          </div>
          <div>
            <div
              class="rounded-[25px] bg-neutral-200 w-full aspect-square cursor-pointer"
            ></div>
          </div>
          <div>
            <div
              class="rounded-[25px] bg-neutral-200 w-full aspect-square cursor-pointer"
            ></div>
          </div>
        </div>
        <button
          class="text-accent uppercase text-2xl mx-auto mt-10 block transition-colors hover:text-black"
        >
          Показать больше
        </button>
      </div>
    </section>
    <Teleport to="body">
      <Transition name="fade">
        <ModalOverlay v-if="true" @click="isShowModal = false">
          <template #content>
            <div class="bg-neutral-100 relative w-[520px] p-12">
              <img
                src="@/assets/svg/close-icon.svg"
                alt="close_icon"
                class="absolute right-4 top-4 w-4 cursor-pointer"
                @click="isShowModal = false"
              />
              <h2 class="uppercase text-2xl font-medium">Обсудить проект</h2>
              <p class="mt-3">
                Если у вас есть какие-либо вопросы или вам нужна помощь в выборе
                наших услуг, пожалуйста, заполните форму обратной связи.
              </p>
              <TheInput placeholder="Ваше имя" />
            </div>
          </template>
        </ModalOverlay>
      </Transition>
    </Teleport>
  </main>
</template>
