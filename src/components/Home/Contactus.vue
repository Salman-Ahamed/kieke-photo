<script setup lang="ts">
import Phone from "../../assets/icons/call.svg";
import Location from "../../assets/icons/location.svg";
import Email from "../../assets/icons/sms.svg";
</script>

<template>
  <section class="py-5">
    <div class="container py-5 px-2 bg-[#F9F5F4]">
      <div class="p-5 flex flex-col md:flex-row gap-10">
        <!-- left side  -->
        <div class="flex-1">
          <!-- header  -->
          <div>
            <h1
              class="uppercase text-[40px] md:text-[48px] lg:text-[54px] leading-[120%] pb-4 font-newYork"
            >
              Getin <span class="text-[#2D3B3BB2]">Touch</span>
            </h1>
            <p
              class="capitalize text-[14px] md:text-[20px] text-[#2D3B3BE5] py-2 font-helvatika"
            >
              We love to hear from you.Our friendly Team is always here to chat.
            </p>
          </div>
          <!-- footer  -->
          <div class="mt-5 space-y-5">
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
        <div class="flex-1">
          <div class="bg-white space-y-5 p-5 w-full">
            <div>
              <input
                type="text"
                placeholder="Leon"
                class="border-b w-[100%] placeholder:text-[20px] py-3 px-2 outline-none border-gray-900"
              />
            </div>
            <div>
              <input
                type="email"
                placeholder="Email Addresh"
                class="border-b w-[100%] placeholder:text-[16px] md:placeholder:[20px] placeholder:text-[#2D3B3BE5] py-3 px-2 outline-none border-gray-400"
              />
            </div>

            <div>
              <textarea
                type="email"
                placeholder="Message"
                class="border-b h-[250px] w-[100%] py-3 px-2 outline-none border-gray-300"
              />
            </div>
            <div>
              <button
                class="bg-[#2D3B3B] w-full py-2 rounded-md text-[#FFFFFF] cursor-pointer font-bold"
              >
                Submit
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
