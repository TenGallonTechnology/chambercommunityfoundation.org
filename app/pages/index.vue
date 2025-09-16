<script setup lang="ts">
import BoardMembers from '~/components/BoardMembers.vue'
import FlexLogoLink from '~/components/FlexLogoLink.vue'

useHead({
  script: [
    {
      src: 'https://widgets.givebutter.com/latest.umd.cjs?acct=Yd0OizzUIrmzC3OR&p=other',
      defer: true
    }
  ]
})
</script>

<template>
  <div>
    <UPageHero
      reverse
      description="Uniting community leaders to build a stronger future through childcare, education, and workforce solutions."
      class="bg-linear-to-t from-white to-primary-50 items-center "
    >
      <img
        src="/1-transparent.png"
        alt="Dublin-Laurens County Chamber Community Foundation"
        class="h-30 md:h-50 w-auto mx-auto"
      >
    </UPageHero>

    <UPageSection
      id="about"
      title="About The Foundation"
      description="The Dublin-Laurens County Chamber Community Foundation exists to support long-term, sustainable community growth. By aligning local leadership with real solutions in the key areas of childcare, education, and workforce development, we are investing in a stronger future for all residents of Laurens County."
      :features="[
        {
          icon: 'i-lucide-baby',
          title: 'Childcare',
          description:
            'By addressing childcare challenges, we help ensure families can thrive and businesses can grow.'
        },
        {
          icon: 'i-lucide-school',
          title: 'Education',
          description:
            'We support educational initiatives that empower our youth and prepare them for future success.'
        },
        {
          icon: 'i-lucide-briefcase',
          title: 'Workforce Solutions',
          description:
            'By fostering workforce development, we create opportunities for all residents to succeed in a changing economy.'
        }
      ]"
    />

    <BoardMembers />

    <UPageSection
      id="childcare"
      title="Childcare"
      description="The Chamber Community Foundation works with our local childcare providers to recruit, retain, improve, and expand local quality care options. "
    />

    <UPageSection
      id="education"
      title="Education"
    >
      <template #description>
        The Chamber Community Foundation works with our local education leaders
        to support efforts in leadership training, exposure to local careers,
        and literacy initiatives. Currently, the Foundation helps recruit
        volunteers for local literacy projects: Read to Lead and Literacy in
        Laurens.
        <UPageLogos>
          <a
            href="https://www.facebook.com/p/READ-to-LEAD-61557373647590/"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img
              src="/RtoL.png"
              alt="Read to Lead"
              class="h-20 w-auto"
            >
          </a>
          <a
            href="https://www.facebook.com/p/Literacy-in-Laurens-100087617144636/"
            target="_blank"
            rel="noopener noreferrer"
          ><img
            src="/literacy-in-laurens.png"
            alt="Literacy in Laurens"
            class="h-20 w-auto"
          ></a>
        </UPageLogos>

        <p class="mt-4">
          The Foundation is proud to announce that Laurens County will be a
          2025-2025 <FlexLogoLink /> Community.
          The Foundational Leadership and Entrepreneurship Experience (FLEX) is
          an entrepreneurship program for any Laurens County high school
          student. Students create and run their own businesses while
          participating in local workshops and mentorship, culminating in a
          Shark Tank style business pitch competition. Our local winner will
          proceed to the state competition, where the state winner receives
          $10,000 cash!
        </p>
        <p class="mt-2">
          Laurens County FLEX Student Application Deadline is <b>October 14, 2025.</b> <UButton
            href="https://form.jotform.com/252535121197151"
            target="_blank"
            rel="noopener noreferrer"
            variant="subtle"
            icon="i-lucide-send"
          >
            Submit your application here
          </UButton>
          <!-- Download file from /flex-student-application -->
          Download the application here:
          <UButton
            href="/flex-student-application.pdf"
            target="_blank"
            rel="noopener noreferrer"
            variant="subtle"
            icon="i-lucide-file-text"
            class="mt-1"
          >
            FLEX Student Application (PDF)
          </UButton>
        </p>
      </template>
    </UPageSection>

    <UPageSection
      id="workforce"
      title="Workforce"
    >
      <template #description>
        The Foundation is proud to present
        <img
          class="h-13 w-auto inline align-bottom"
          alt="Aim 2 Summit"
          src="/Aim2SummitTrimmed.png"
        >, A one-day interactive and educational exposition featuring leaders
        in AI, automation, innovation, manufacturing, & mechatronics. Save the
        Date! October 2, 2025 at OFTC. FREE to attend! Interested in attending
        as a group or becoming an exhibitor? Email
        <a
          class="text-primary"
          href="mailto:aim2summit@gmail.com"
        >aim2summit@gmail.com</a>
        for more details.
      </template>
    </UPageSection>

    <UPageSection id="donate">
      <UPageCTA
        title="Donate"
        description="Dublin-Laurens County Chamber Community is a 501c3 non-profit. "
        variant="subtle"
      >
        <span class="text-primary text-center mt-0">Your tax-deductible donation to the Foundation can be mailed to: 1200 Bellevue Ave, Dublin, GA 31021</span>

        <!-- Givebutter Donation Widget -->
        <givebutter-widget id="L07Zyj" class="mx-auto"></givebutter-widget>

        Contact us
        <UButton
          href="mailto:info@chambercommunityfoundation.org"
          icon="i-lucide-mail"
          variant="subtle"
        >
          info@chambercommunityfoundation.org
        </UButton>
      </UPageCTA>
    </UPageSection>
  </div>
</template>
