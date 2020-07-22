<template>
  <div class="flex flex-col w-screen h-full">
    <!-- Your name, profile picture and contact -->
    <HeadWrapper
      name="Sharon"
      title="Student"
      userImgURL="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcREShpe_KRE3fBwhVKV3uHUrt661DCFiIUm7Q&usqp=CAU"
      phone="+60123456789"
      email="xxSharonWong@gmail.com"
    />
    <!-- About Me -->
    <AboutWrapper
      aboutMe="I'm a singer and dancer. Muakkkskksks"
      linkedInURL
      languages="Chinese, English"
      nationality="Taiwanese"
      interest="Delon"
    />
    <!-- Working Experience -->
    <CareerWrapper>
      <template v-slot:career>
        <Career companyName="青春有你" title="实习生" startDate="01-01-2020" endDate="NA">
          <!-- List of what you had did in the company -->
          <template v-slot:experience>
            <ul class="text-gray-600 list-inside list-disc mt-2 px-4"></ul>
          </template>
        </Career>
      </template>
    </CareerWrapper>
    <!-- Achievement -->
    <AchievementWrapper project="2" client="7800000000" award="10000"/>
    <!-- Portfolio -->
    <PortfolioWrapper>
      <template v-slot:portfolio>
        <div class="grid grid-cols-1 md:grid-cols-3">
          <ProjectCard
            imgUrl="../img/github.png"
            name="青春有你"
            project="123"
            projectURL="https://github.com"
          />/>
        </div>
      </template>
    </PortfolioWrapper>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Sharon Wong"
    };
  }
};
</script>