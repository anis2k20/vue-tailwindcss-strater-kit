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
          class="hero-badge text-xs inline-flex items-center gap-2 px-1.5 pr-4 py-1 bg-white/6 border border-white/10 rounded-full text-12 text-white/85 w-fit mb-6 backdrop-blur-8"
        >
          <strong
            class="bg-brand-500 text-white text-[12px] px-2.5 py-0.5 rounded-full  tracking-wide font-semibold"
          >
            SECURE</strong
          >

          Account recovery in 3 simple steps
        </div>
        <h1 class="text-5xl leading-tight font-semibold -tracking-0.025 mb-4">
          Forgot your password?<br />
          <span
            class="bg-linear-to-r from-brand-200 to-brand-400 bg-clip-text text-transparent italic font-normal"
            >We've got you.</span
          >
        </h1>
        <p class="text-15 leading-relaxed text-white/72 max-w-115 mb-7">
          Reset your SaltSync Care password securely. We'll send a verification
          code to your registered mobile or email — no waiting, no hassle.
        </p>

        <!-- Connection Card -->
        <div
          class="conn-card rounded-2xl p-4.5 backdrop-blur-12 mb-6 relative overflow-hidden"
        >
          <div
            class="absolute top-0 left-0 right-0 h-px bg-linear-to-r from-transparent via-white/30 to-transparent"
          ></div>

          <!-- Speed Row -->
          <div class="tips-header">
            <span class="tips-title">
              <svg
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
              >
                <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z" />
              </svg>
              STAY SAFE
            </span>
          </div>
          <div class="tips-list">
            <div class="tip-row">
              <div class="tip-icon">
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.5"
                >
                  <path d="M20 6L9 17l-5-5" />
                </svg>
              </div>
              <span
                ><strong>SaltSync never asks for your password</strong>Our team
                won't call asking you to share OTP codes or passwords.</span
              >
            </div>
            <div class="tip-row">
              <div class="tip-icon">
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.5"
                >
                  <path d="M20 6L9 17l-5-5" />
                </svg>
              </div>
              <span
                ><strong>Codes expire in 10 minutes</strong>Verification codes
                are single-use and time-limited for security.</span
              >
            </div>
            <div class="tip-row">
              <div class="tip-icon">
                <svg
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.5"
                >
                  <path d="M20 6L9 17l-5-5" />
                </svg>
              </div>
              <span
                ><strong>Need help? Call us directly</strong>Khulna-based
                support, available 24/7 at our hotline below.</span
              >
            </div>
          </div>

          <!-- Service List -->
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
        <div class="text-brand-200">24/7 Hotline · 09638-666999</div>
      </footer>
    </aside>

    <!-- Right Auth Panel -->
    <div class="p-10 flex flex-col justify-between">
      <!-- Auth top -->
      <div class="auth-top flex justify-between items-center">
        <div class="top-link text-13 text-secondary">
          <a href="#" class="text-brand-800 text-xs"
            ><ArrowLeft size="16" class="inline-flex mb-1" /> Back to sign in</a
          >
        </div>
        <div class="top-controls flex items-center gap-3 text-[12px]">
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
              >Account recovery</span
            >
          </div>

          <!-- Greeting -->
          <div class="form-greeting">
            <h2 class="form-title text-3xl font-semibold text-primary mb-2">
              Reset your password
            </h2>
            <p class="form-sub text-gray-500 text-[14px]">
              Enter your Customer ID or registered email/mobile. We'll send a
              verification code.
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

              <!-- Submit Button -->
              <button
                type="submit"
                class="submit-btn w-full px-4 py-3 bg-brand-600 text-white rounded-lg font-medium text-14 shadow-btn hover:shadow-btn-hover hover:bg-brand-accent-hover transition-all duration-200 relative overflow-hidden border-none cursor-pointer"
              >
                <span
                  class="relative z-10 flex items-center justify-center gap-2"
                >
                  Send verification code <ArrowRight size="16" />
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

              <!-- Submit Button -->
              <button
                type="submit"
                class="submit-btn w-full px-4 py-3 bg-brand-600 text-white rounded-lg font-medium text-14 shadow-btn hover:shadow-btn-hover hover:bg-brand-accent-hover transition-all duration-200 relative overflow-hidden border-none cursor-pointer"
              >
                <span
                  class="relative z-10 flex items-center justify-center gap-2"
                >
                  Send verification code <ArrowRight size="16" />
                </span>
              </button>
            </form>
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
import {
  ArrowLeft,
  ArrowRight,
  Eye,
  EyeOff,
  IdCard,
  Mail,
} from "lucide-vue-next";

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

/* forgot password */

.tips-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 14px;
}

.tips-title {
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: rgba(255, 255, 255, 0.5);
  font-family: "Geist Mono", monospace;
  font-weight: 500;
  display: flex;
  align-items: center;
  gap: 8px;
}

.tips-title svg {
  width: 14px;
  height: 14px;
  color: var(--brand-300);
}

.tips-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.tip-row {
  display: flex;
  align-items: flex-start;
  gap: 10px;
  font-size: 13px;
  color: rgba(255, 255, 255, 0.85);
  line-height: 1.5;
}

.tip-icon {
  width: 20px;
  height: 20px;
  border-radius: 6px;
  background: rgba(80, 135, 228, 0.2);
  border: 1px solid rgba(80, 135, 228, 0.3);
  display: grid;
  place-items: center;
  flex-shrink: 0;
  color: var(--brand-200);
  margin-top: 1px;
}
.tip-icon svg {
  width: 11px;
  height: 11px;
}

.tip-row strong {
  color: white;
  font-weight: 500;
  display: block;
  margin-bottom: 2px;
}
</style>
