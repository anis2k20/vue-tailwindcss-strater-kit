<template>
  <!-- grid-cols-[1.1fr_1fr] -->
  <div
    class="grid xl:grid-cols-2 min-h-screen font-geist"
    :data-theme="'theme_1'"
    :data-mode="themeMode"
  >
    <!-- Left brand Panel -->
    <aside
      class="brand-panel relative hidden xl:flex flex-col px-11 py-8 text-white overflow-hidden transition-colors duration-300"
    >
      <!-- Background gradient -->
      <div
        class="absolute inset-0 bg-linear-to-br from-brand-700 to-brand-900"
      ></div>
      <!-- Grid overlay -->
      <div
        class="absolute inset-0 opacity-40"
        style="
          background-image:
            linear-gradient(
              90deg,
              rgba(255, 255, 255, 0.1) 1px,
              transparent 1px
            ),
            linear-gradient(0deg, rgba(255, 255, 255, 0.1) 1px, transparent 1px);
          background-size: 56px 56px;
          mask-image: radial-gradient(
            ellipse 80% 70% at 30% 50%,
            black 30%,
            transparent 80%
          );
        "
      ></div>

      <!-- Signal rings -->
      <div class="signal-rings absolute bottom-15 right-8 w-50 h-50">
        <div
          class="signal-ring absolute inset-0 border-2 border-brand-300 rounded-full animate-pulse"
        ></div>
        <div
          class="signal-ring absolute inset-0 border-2 border-brand-300 rounded-full animate-pulse"
          style="animation-delay: 1s"
        ></div>
        <div
          class="signal-ring absolute inset-0 border-2 border-brand-300 rounded-full animate-pulse"
          style="animation-delay: 2s"
        ></div>
      </div>

      <!-- Floating orbs -->
      <div
        class="orb orb-1 absolute blur-3xl opacity-55 rounded-full bg-brand-500 -top-25 left-15 w-80 h-80"
      ></div>
      <div
        class="orb orb-2 absolute blur-3xl opacity-55 rounded-full bg-brand-400 bottom-5 -right-15 w-65 h-65"
      ></div>

      <!-- brand Header -->
      <header
        class="brand-header relative z-10 flex justify-between items-center"
      >
        <div
          class="logo-wrap flex items-center gap-3 bg-white/95 px-4 py-2 rounded-xl shadow-lg"
        >
          <!-- <img src="/logo.png" alt="SaltSync" class="h-8 w-auto" /> -->
          <div class="logo-divider w-px h-4.5 bg-gray-300"></div>
          <span
            class="logo-tag text-13 font-semibold text-brand-700 tracking-wide"
            >Care</span
          >
        </div>
        <div
          class="status-pill inline-flex items-center gap-2 text-xs px-3 py-1.5 bg-white/6 border border-white/10 rounded-full text-12 text-white/85 backdrop-blur-8"
        >
          <div
            class="status-dot w-2 h-2 rounded-full bg-success-400 shadow-success-400 animate-pulse"
          ></div>
          Network operational · Khulna
        </div>
      </header>

      <!-- Hero -->
      <div
        class="brand-hero relative z-10 flex-1 flex flex-col justify-center max-w-150 py-7"
      >
        <div
          class="hero-badge inline-flex items-center gap-2 px-1.5 pr-4 py-1 bg-white/6 border border-white/10 rounded-full text-12 text-white/85 w-fit mb-6 backdrop-blur-8"
        >
          <strong
            class="bg-brand-500 text-white text-[12px] px-2.5 py-0.5 rounded-full text-10 tracking-wide font-semibold"
          >
            FIBER</strong
          >

          Khulna's trusted internet provider
        </div>
        <h1 class="text-5xl leading-tight font-semibold -tracking-0.025 mb-4">
          Your connection,<br />
          <span
            class="bg-linear-to-r from-brand-200 to-brand-400 bg-clip-text text-transparent italic font-normal"
            >your control.</span
          >
        </h1>
        <p class="text-15 leading-relaxed text-white/72 max-w-115 mb-7">
          Manage your SaltSync internet account — pay bills, check usage,
          upgrade packages, and get instant support, all in one place.
        </p>

        <!-- Connection Card -->
        <div
          class="conn-card  rounded-2xl p-4.5 backdrop-blur-12 mb-6 relative overflow-hidden"
        >
          <div
            class="absolute top-0 left-0 right-0 h-px bg-linear-to-r from-transparent via-white/30 to-transparent"
          ></div>
          <div class="conn-header flex justify-between items-center mb-3.5">
            <span
              class="conn-title text-sm uppercase tracking-wider text-white font-medium font-mono"
              >Connection Status</span
            >
            <div
              class="conn-live flex items-center gap-1.5 text-xs text-success-400 font-mono"
            >
              <div
                class="w-1.25 h-1.25 rounded-full  bg-success-400 shadow-success-400 animate-pulse"
              ></div>
              ONLINE
            </div>
          </div>

          <!-- Speed Row -->
          <div class="speed-row grid grid-cols-2 gap-3.5 mb-3.5">
            <div
              class="speed-stat bg-white/3 border border-white/6 rounded-xl p-3 px-4"
            >
              <div
                class="speed-label flex items-center gap-1.5 text-10 uppercase tracking-wide text-white/55 font-mono mb-1.5"
              >
                <svg
                  width="11"
                  height="11"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path
                    d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"
                  />
                </svg>
                Download
              </div>
              <div
                class="speed-value text-22 font-semibold text-white -tracking-0.02 font-geist"
              >
                1.2<small
                  class="text-11 font-normal text-white ml-0.75 font-mono"
                  >Gbps</small
                >
              </div>
              <div
                class="speed-bar h-0.75 bg-white/8 rounded mt-2 overflow-hidden"
              >
                <div
                  class="speed-fill h-full bg-gradient-to-r from-brand-400 to-brand-200 rounded animate-pulse"
                ></div>
              </div>
            </div>
            <div
              class="speed-stat bg-white/3 border border-white/6 rounded-xl p-3 px-4"
            >
              <div
                class="speed-label flex items-center gap-1.5 text-10 uppercase tracking-wide text-white/55 font-mono mb-1.5"
              >
                <svg
                  width="11"
                  height="11"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path
                    d="M12 22L2 17l10-5 10 5-10 5zM2 7l10-5 10 5M12 12l10-5"
                  />
                </svg>
                Upload
              </div>
              <div
                class="speed-value text-22 font-semibold text-white -tracking-0.02 font-geist"
              >
                500<small
                  class="text-11 font-normal text-white ml-0.75 font-mono"
                  >Mbps</small
                >
              </div>
              <div
                class="speed-bar h-0.75 bg-white rounded mt-2 overflow-hidden"
              >
                <div
                  class="speed-fill h-full bg-gradient-to-r from-brand-400 to-brand-200 rounded animate-pulse"
                ></div>
              </div>
            </div>
          </div>

          <!-- Service List -->
          <div class="service-list flex flex-col gap-1.5">
            <div
              class="service-row flex items-center gap-2.5 p-2 px-2.5 bg-white/2 rounded-7 text-12 text-white/85"
            >
              <div
                class="service-icon fiber rounded grid place-items-center flex-shrink-0 text-white bg-brand-300/25"
              >
                <svg
                  width="11"
                  height="11"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path d="M12 2L2 7l10 5 10-5-10-5z" />
                </svg>
              </div>
              <span class="flex-1">Fiber Optic Network</span>
              <span
                class="service-status font-mono text-xs text-10 text-success-400 tracking-wide"
                >ACTIVE</span
              >
            </div>
            <div
              class="service-row flex items-center gap-2.5 p-2 px-2.5 bg-white/2 rounded-7 text-12 text-white/85"
            >
              <div
                class="service-icon wifi rounded grid place-items-center shrink-0 text-success-400 bg-success-400/2"
              >
                <svg
                  width="11"
                  height="11"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path
                    d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2z"
                  />
                </svg>
              </div>
              <span class="flex-1">Wi-Fi Hotspot</span>
              <span
                class="service-status font-mono text-10 text-success-400 tracking-wide text-xs"
                >ACTIVE</span
              >
            </div>
            <div
              class="service-row flex items-center gap-2.5 p-2 px-2.5 bg-white/2 rounded-7 text-12 text-white/85"
            >
              <div
                class="service-icon support rounded grid place-items-center shrink-0 text-warning-500 bg-warning-500/2"
              >
                <svg
                  width="11"
                  height="11"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path
                    d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2z"
                  />
                </svg>
              </div>
              <span class="flex-1">24/7 Support</span>
              <span
                class="service-status font-mono text-10 text-success-400 tracking-wide text-xs"
                >AVAILABLE</span
              >
            </div>
          </div>
        </div>
      </div>

      <!-- brand Footer -->
      <footer
        class="brand-footer relative z-10 pt-6 text-xs border-t border-white/8 flex justify-between items-center text-11 text-white/5"
      >
        <div class="support-info flex items-center gap-2">
          <a href="#" class="text-brand-200 no-underline font-mono font-medium"
            >support@saltsync.com</a
          >
        </div>
        <div class="text-brand-200">© 2024 SaltSync</div>
      </footer>
    </aside>

    <!-- Right Auth Panel -->
    <div class="p-10 flex flex-col justify-between">
      <!-- Auth top -->
      <div class="auth-top flex justify-between items-center">
        <div
          class="secure-pill text-[12px] inline-flex items-center gap-2 px-3 py-1.5 bg-pill border border-gray-200 rounded-full text-12 text-secondary transition-colors duration-300"
        >
          <svg
            width="12"
            height="12"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            class="text-success-600"
          >
            <path
              d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
            />
          </svg>
          Secure Connection
        </div>
        <div class="top-controls flex items-center gap-3 text-[12px]">
          <div class="top-link text-13 text-secondary">
            New customer?
            <a href="#" class="text-brand-800 no-underline font-medium ml-1"
              >Check coverage</a
            >
          </div>
          <button
            @click="toggleTheme"
            class="theme-toggle w-9.5 h-9.5 bg-pill border border-gray-200 bg-gray-50 rounded-xl grid place-items-center text-secondary transition-all duration-200 hover:border-brand-accent hover:text-brand-accent relative overflow-hidden"
          >
            <svg
              width="16"
              height="16"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              class="icon-sun absolute transition-all duration-300"
              :class="
                themeMode === 'dark'
                  ? 'opacity-0 rotate-90 scale-50'
                  : 'opacity-100 rotate-0 scale-100'
              "
            >
              <circle cx="12" cy="12" r="5" />
              <path
                d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"
              />
            </svg>
            <svg
              width="16"
              height="16"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              class="icon-moon absolute transition-all duration-300"
              :class="
                themeMode === 'dark'
                  ? 'opacity-100 rotate-0 scale-100'
                  : 'opacity-0 -rotate-90 scale-50'
              "
            >
              <path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z" />
            </svg>
          </button>
        </div>
      </div>
      <main
        class="auth-panel bg-surface flex flex-col items-center px-11 py-7 relative transition-colors duration-300"
      >
        <!-- Form Wrapper -->
        <div
          class="auth-form-wrap flex-1 flex flex-col justify-center max-w-100 space-y-4"
        >
          <!-- welcome -->
          <div class="flex itmes-center text-center gap-2">
            <div class="bg-brand-800 w-10 h-px"></div>
            <span class="leading-0 text-[12px] font-medium text-brand-900"
              >Welcome to SaltSync Care</span
            >
          </div>

          <!-- Greeting -->
          <div class="form-greeting">
            <h2 class="form-title text-3xl font-semibold text-primary mb-2">
              Sign in to your account
            </h2>
            <p class="form-sub text-gray-500 text-[14px]">
              Use your Customer ID or email/mobile to manage your internet
              service.
            </p>
          </div>

          <!-- Method Tabs -->
          <div
            class="method-tabs flex gap-2 bg-gray-200 p-1.5 rounded-lg mt-2 mb-6"
          >
            <button
              @click="activeTab = 'cid'"
              :class="[
                'tab-btn flex-1 flex items-center px-4 py-2 text-sm font-medium rounded-lg transition-colors duration-200 cursor-pointer',
                activeTab === 'cid'
                  ? 'active bg-white text-brand-900 shadow-sm'
                  : 'text-gray-600 hover:bg-gray-200',
              ]"
            >
              <IdCard size="16" class="mr-1" />
              Customer ID
            </button>
            <button
              @click="activeTab = 'email'"
              :class="[
                'tab-btn flex-1 flex items-center px-4 py-2 text-sm font-medium rounded-lg transition-colors duration-200 cursor-pointer',
                activeTab === 'email'
                  ? 'active bg-white text-brand-900 shadow-sm'
                  : ' text-gray-600 hover:bg-gray-200',
              ]"
            >
              <Mail size="16" class="mr-1" />
              Email or Mobile
            </button>
          </div>

          <!-- email tab -->
          <div v-show="activeTab === 'email'" class="tab-content block">
            <form @submit.prevent="handleSubmit">
              <!-- Email Field -->
              <div class="field mb-4">
                <label class="flex justify-between text-xs mb-2 text-gray-500">
                  <span class="font-medium text-primary"
                    >Email or mobile number</span
                  >
                </label>
                <div
                  class="relative text-sm flex items-center border py-2.5 px-3 border-gray-300 rounded-lg bg-input overflow-hidden focus-within:border-brand-accent transition-colors duration-200"
                >
                  <input
                    type="email"
                    v-model="email"
                    placeholder="Enter your email"
                    class="input-field flex-1 bg-transparent border-none outline-none placeholder-muted"
                    required
                  />
                </div>
              </div>

              <!-- Password Field -->
              <div class="field mb-4">
                <label class="flex justify-between text-xs mb-2 text-gray-500">
                  <span class="font-medium">Password</span>
                  <a href="#" class="text-brand-600 font-semibold">Forgot?</a>
                </label>
                <div
                  class="input-wrap relative flex items-center border border-gray-300 rounded-lg bg-input px-3 py-2.5 focus-within:border-brand-accent transition-colors duration-200"
                >
                  <input
                    :type="showPassword ? 'text' : 'password'"
                    v-model="password"
                    placeholder="Enter your password"
                    class="input-field flex-1 text-sm bg-transparent border-none outline-none text-primary placeholder-muted"
                    required
                  />
                  <button
                    type="button"
                    @click="showPassword = !showPassword"
                    class="ml-2"
                  >
                    <Eye size="16" class="text-gray-500" v-if="showPassword" />
                    <EyeOff size="16" class="text-gray-500" v-else />
                  </button>
                </div>
              </div>

              <!-- Options -->
              <div class="row-options flex justify-between items-center mb-6">
                <label class="checkbox flex items-center gap-2 cursor-pointer">
                  <input
                    type="checkbox"
                    v-model="rememberMe"
                    class="appearance-none h-4 w-4 rounded border border-gray-400 checked:bg-brand-500 checked:border-brand-500"
                  />

                  <span class="text-sm text-gray-500">Keep me signed in</span>
                </label>
              </div>

              <!-- Submit Button -->
              <button
                type="submit"
                class="submit-btn w-full px-4 py-3 bg-brand-600 text-white rounded-lg font-medium text-14 shadow-btn hover:shadow-btn-hover hover:bg-brand-accent-hover transition-all duration-200 relative overflow-hidden border-none cursor-pointer"
              >
                <span
                  class="relative z-10 flex items-center justify-center gap-2"
                >
                  Sign In <ArrowRight size="16" />
                </span>
              </button>
            </form>
          </div>

          <!-- cid tab -->
          <div v-show="activeTab === 'cid'" class="tab-content block">
            <form @submit.prevent="handleSubmit">
              <!-- CID Field -->
              <div class="field mb-4">
                <label class="flex justify-between text-xs mb-2 text-gray-500">
                  <span class="font-medium text-primary"
                    >Customer ID (CID)</span
                  >
                  <span>SS-XXXX</span>
                </label>
                <div
                  class="relative text-sm flex items-center border border-gray-300 rounded-lg bg-input overflow-hidden focus-within:border-brand-accent transition-colors duration-200"
                >
                  <div
                    class="bg-brand-100 px-3 py-2.5 font-semibold text-brand-700"
                  >
                    SS -
                  </div>
                  <input
                    type="text"
                    v-model="cid"
                    @input="cid = cid.replace(/\D/g, '')"
                    placeholder="Enter your CID"
                    class="input-field flex-1 pl-2 bg-transparent border-none outline-none text-primary placeholder-muted"
                    required
                  />
                </div>
              </div>

              <!-- Password Field -->
              <div class="field mb-4">
                <label class="flex justify-between text-xs mb-2 text-gray-500">
                  <span class="font-medium text-primary">Password</span>
                  <a href="#" class="text-brand-600 font-semibold">Forgot?</a>
                </label>
                <div
                  class="input-wrap relative flex items-center border border-gray-300 rounded-lg bg-input px-3 py-2.5 focus-within:border-brand-accent transition-colors duration-200"
                >
                  <input
                    :type="showPassword ? 'text' : 'password'"
                    v-model="password"
                    placeholder="Enter your password"
                    class="input-field flex-1 text-sm bg-transparent border-none outline-none text-primary placeholder-muted"
                    required
                  />
                  <button
                    type="button"
                    @click="showPassword = !showPassword"
                    class="ml-2"
                  >
                    <Eye size="16" class="text-gray-500" v-if="showPassword" />
                    <EyeOff size="16" class="text-gray-500" v-else />
                  </button>
                </div>
              </div>

              <!-- Options -->
              <div class="row-options flex justify-between items-center mb-6">
                <label class="checkbox flex items-center gap-2 cursor-pointer">
                  <input
                    type="checkbox"
                    v-model="rememberMe"
                    class="appearance-none h-4 w-4 rounded border border-gray-400 checked:bg-brand-500 checked:border-brand-500"
                  />

                  <span class="text-sm text-gray-500">Keep me signed in</span>
                </label>
              </div>

              <!-- Submit Button -->
              <button
                type="submit"
                class="submit-btn w-full px-4 py-3 bg-brand-600 text-white rounded-lg font-medium text-14 shadow-btn hover:shadow-btn-hover hover:bg-brand-accent-hover transition-all duration-200 relative overflow-hidden border-none cursor-pointer"
              >
                <span
                  class="relative z-10 flex items-center justify-center gap-2"
                >
                  Sign In <ArrowRight size="16" />
                </span>
              </button>
            </form>
          </div>

          <!-- Quick Action -->
          <div
            class="rounded-lg bg-gray-50 border border-dashed border-gray-300 p-3 text-xs flex justify-between"
          >
            <span class="text-gray-500">Just want to pay your bill?</span>
            <a href="#" class="text-brand-600 font-semibold ml-1"
              >Quick Pay
              <ArrowRight size="16" class="inline-block ml-1" />
            </a>
          </div>

          <!-- Divider -->
          <div class="divider relative flex items-center">
            <div class="flex-1 h-px bg-gray-200"></div>
            <span
              class="px-4 text-14 text-muted bg-surface text-xs text-gray-400"
              >Or continue with</span
            >
            <div class="flex-1 h-px bg-gray-200"></div>
          </div>

          <!-- Social -->
          <div class="social-stack flex gap-3">
            <button
              class="flex-1 flex items-center justify-center gap-2 px-4 py-2.5 bg-gray-50 border border-gray-200 rounded-lg text-14 text-secondary font-medium hover:bg-gray-100 transition-colors duration-200"
            >
              <img
                src="https://img.icons8.com/?size=100&id=V5cGWnc9R4xj&format=png&color=000000"
                alt="Twitter"
                class="w-5 h-5 rounded-full"
              />
              Google
            </button>
            <button
              class="flex-1 flex items-center justify-center gap-2 px-4 py-2.5 bg-gray-50 border border-gray-200 rounded-lg text-14 text-secondary font-medium hover:bg-gray-100 transition-colors duration-200"
            >
              <img
                src="https://img.icons8.com/?size=100&id=uLWV5A9vXIPu&format=png&color=000000"
                alt="Facebook"
                class="w-5 h-5 rounded-full"
              />

              Facebook
            </button>
          </div>

          <!-- Bottom Note -->
          <div class="text-center mt-6 text-xs text-gray-500">
            Don't have an account?

            <a href="#" class="text-brand-700 hover:underline"
              >Contact SaltSync</a
            >.
          </div>
        </div>
      </main>

      <div
        class="flex justify-between items-center text-xs text-gray-500 border-t border-gray-200 pt-4"
      >
        <p>v4.2.18 · care.saltsync.com</p>
        <div>
          <a href="#" class="mr-4 text-gray-500 hover:text-gray-800">Privacy</a>
          <a href="#" class="mr-4 text-gray-500 hover:text-gray-800">Terms</a>
          <a href="#" class="text-gray-500 hover:text-gray-800">Help</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { ArrowRight, Eye, EyeOff, IdCard, Mail } from "lucide-vue-next";

const activeTab = ref("email");
const themeMode = ref("light");
const email = ref("");
const password = ref("");
const cid = ref("");
const rememberMe = ref(false);
const showPassword = ref(false);
</script>

<style scoped>
/* Custom animations and styles that can't be done with Tailwind */
.signal-rings .signal-ring {
  animation: signal 3s ease-out infinite;
}

.signal-rings .signal-ring:nth-child(2) {
  animation-delay: 1s;
}

.signal-rings .signal-ring:nth-child(3) {
  animation-delay: 2s;
}

@keyframes signal {
  0% {
    transform: scale(0.3);
    opacity: 1;
  }
  100% {
    transform: scale(1.5);
    opacity: 0;
  }
}

.speed-fill {
  animation: fill 2.5s ease-out;
}

@keyframes fill {
  from {
    width: 0;
  }
  to {
    width: 80%;
  } /* Example width */
}

.tab-content {
  animation: fadeIn 0.25s ease;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.conn-card {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 14px;
  padding: 18px;
  backdrop-filter: blur(12px);
  margin-bottom: 24px;
  position: relative;
  overflow: hidden;
}
</style>
