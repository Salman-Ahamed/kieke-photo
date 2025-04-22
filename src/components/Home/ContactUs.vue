<script setup lang="ts">
import Phone from "../../assets/icons/call.svg";
import Location from "../../assets/icons/location.svg";
import Email from "../../assets/icons/sms.svg";
</script>

<template>
  <section class="py-5 sm:py-10 lg:py-20 px-5 sm:px-10 lg:px-16" id="contact">
    <div class="container p-5 sm:p-10 lg:p-16 bg-[#F9F5F4]">
      <div class="grid grid-cols-1 md:grid-cols-12 gap-24">
        <!-- left side  -->
        <div class="col-span-1 md:col-span-5 w-full">
          <!-- header  -->
          <div>
            <h1
              class="uppercase text-[40px] md:text-[48px] lg:text-[54px] leading-[120%] pb-4 font-newYork"
            >
              Getin <span class="text-[#2D3B3BB2]">Touch</span>
            </h1>
            <p
              class="capitalize text-sm md:text-xl max-w-[500px] text-[#2D3B3BE5] py-2 font-helvatika"
            >
              We love to hear from you.Our friendly Team is always here to chat.
            </p>
          </div>
          <!-- footer  -->
          <div
            class="mt-5 sm:mt-10 lg:mt-16 space-y-5 md:space-y-8 xl:space-y-12"
          >
            <div class="flex gap-4 items-center">
              <div class="p-3 rounded-md bg-white w-[60px] h-[60px]">
                <img :src="Location" alt="" />
              </div>
              <div>
                <h1
                  class="text-[16px] md:text-[24px] uppercase font-newYork text-[#2D3B3B]"
                >
                  Location
                </h1>
                <p
                  class="text-[#2D3B3BE5] capitalize text-[14px] md:text-[20px]"
                >
                  199 Nueces ST,Austin,TX 78701
                </p>
              </div>
            </div>
            <div class="flex gap-4 items-center">
              <div class="p-3 rounded-md bg-white w-[60px] h-[60px]">
                <img :src="Phone" alt="" />
              </div>
              <div>
                <h1
                  class="text-[16px] md:text-[24px] uppercase font-newYork text-[#2D3B3B]"
                >
                  Phone
                </h1>
                <p
                  class="text-[#2D3B3BE5] capitalize text-[14px] md:text-[20px]"
                >
                  +1(456)666-4077
                </p>
              </div>
            </div>
            <div class="flex gap-4 items-center">
              <div class="p-3 rounded-md bg-white w-[60px] h-[60px]">
                <img :src="Email" alt="" />
              </div>
              <div>
                <h1
                  class="text-[16px] md:text-[24px] uppercase font-newYork text-[#2D3B3B]"
                >
                  Email
                </h1>
                <p
                  class="text-[#2D3B3BE5] capitalize text-[14px] md:text-[20px]"
                >
                  support@free.com
                </p>
              </div>
            </div>
          </div>
        </div>
        <!-- Right side  -->
        <div class="col-span-1 md:col-span-7 p-8 bg-white space-y-5 2xl:ml-10">
          <div>
            <input
              type="text"
              placeholder="Leon"
              class="border-b bg-[#F5F5F54D] w-full placeholder:text-[20px] p-6 outline-none border-gray-900"
            />
          </div>
          <div>
            <input
              type="email"
              placeholder="Email Addresh"
              class="border-b w-full placeholder:text-[16px] bg-[#F5F5F54D] md:placeholder:[20px] placeholder:text-[#2D3B3BE5] p-6 outline-none border-gray-400"
            />
          </div>

          <div>
            <textarea
              type="email"
              placeholder="Message"
              class="border-b h-[250px] lg:h-[303px] bg-[#F5F5F54D] w-full p-6 outline-none border-gray-300"
            />
          </div>
          <div>
            <button
              class="bg-[#2D3B3B] w-full py-6 text-[#FFFFFF] cursor-pointer font-medium text-xl"
            >
              Submit
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
