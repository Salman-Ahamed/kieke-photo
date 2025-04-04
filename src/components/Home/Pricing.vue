<script setup lang="ts">
import TickCirle from "../../assets/icons/tick-circle.svg";
</script>

<template>
  <section class="py-10">
    <div class="container px-2">
      <!-- heading  -->
      <div class="text-center">
        <h1
          class="text-[#2D3B3B] uppercase text-[40px] md:text-[48px] lg:text-[54px] leading-[120%] font-newYork"
        >
          Pricings
        </h1>
        <p
          class="text-[16px] md:text-[20px] capitalize text-[#2D3B3BE5] py-4 font-helvatika"
        >
          Let’s craft something exceptional—because your moments deserve nothing
          less.
        </p>
      </div>
      <!-- -------- body ----------- -->
      <div class="mt-5">
        <div class="h-[20px] bg-gray-200 rounded-sm relative">
          <div
            class="h-[20px] absolute top-0 left-0 bg-[#2D3B3B] min-w-[200px] max-w-[300px] w-[100%]"
          >
            <div
              class="w-[100px] flex items-center justify-center text-[16px] md:text-[23px] leading-[150%] text-center text-[#FFFFFF] font-[500] h-[40px] bg-[#2D3B3B] absolute -top-[50%] -right-[10%]"
            >
              $244
            </div>
          </div>
        </div>
        <div class="mt-3">
          <div class="flex justify-between">
            <h1
              class="text-[16px] md:text-[23px] leading-[150%] text-center text-[#2D3B3B] font-[500]"
            >
              $0
            </h1>
            <h1
              class="text-[16px] md:text-[23px] leading-[150%] text-center text-[#2D3B3B] font-[500]"
            >
              $1,000
            </h1>
          </div>
        </div>
        <div
          class="bg-[#F9F5F4] mt-5 py-8 flex lg:items-center px-2 flex-col lg:flex-row gap-5"
        >
          <!-- left side  -->
          <div class="flex-[0.8] space-y-3 md:space-y-">
            <div class="flex items-center gap-2">
              <img :src="TickCirle" alt="" />
              <h1
                class="text-[14px] capitalize md:text-[18px] text-[#2D3B3B] font-helvatika"
              >
                Take very less time
              </h1>
            </div>
            <div class="flex items-center gap-2">
              <img :src="TickCirle" alt="" />
              <h1
                class="text-[14px] capitalize md:text-[18px] text-[#2D3B3B] font-helvatika"
              >
                you get Advanced edited digital
              </h1>
            </div>
            <div class="flex items-center gap-2">
              <img :src="TickCirle" alt="" />
              <h1
                class="text-[14px] capitalize md:text-[18px] text-[#2D3B3B] font-helvatika"
              >
                files in large format
              </h1>
            </div>
          </div>
          <!-- right side  -->
          <div
            class="flex-[1.2] flex flex-col gap-4 text-center sm:text-start sm:flex-row w-full justify-between p-8 bg-[#2D3B3B]"
          >
            <div class="p-3">
              <div>
                <h1
                  class="uppercase text-[#FFFFFF] font-newYork text-[34px] md:text-[40px] leading-[120%]"
                >
                  $244
                </h1>
                <p
                  class="capitalize text-[16px] md:text-[20px] font-helvatika text-[#FFFFFF]"
                >
                  Total Amount
                </p>
              </div>
            </div>
            <div class="bg-white text-black p-3">
              <div>
                <h1
                  class="uppercase font-newYork text-[34px] md:text-[40px] leading-[120%]"
                >
                  $244
                </h1>
                <p class="capitalize text-[16px] md:text-[20px] font-helvatika">
                  Total Amount
                </p>
              </div>
            </div>
            <div class="p-3">
              <div>
                <h1
                  class="uppercase text-[#FFFFFF] font-newYork text-[34px] md:text-[40px] leading-[120%]"
                >
                  $244
                </h1>
                <p
                  class="capitalize text-[16px] md:text-[20px] font-helvatika text-[#FFFFFF]"
                >
                  Total Amount
                </p>
              </div>
            </div>
            <div class="p-3">
              <div>
                <h1
                  class="uppercase text-[#FFFFFF] font-newYork text-[34px] md:text-[40px] leading-[120%]"
                >
                  $244
                </h1>
                <p
                  class="capitalize text-[16px] md:text-[20px] font-helvatika text-[#FFFFFF]"
                >
                  Total Amount
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
