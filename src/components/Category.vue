<template>
    <v-item-group mandatory class="mt-n1" >
      <v-container>
        <v-row justify="center" class="space">
          <v-col
            cols="12"
            xs="12"
            sm="4"
            md="2"
            v-for="(category, i) in categories"
            :key="i"
          >
            <v-item>
              <v-card
                :color="category.active ? '#D5F0DB' : 'white'"
                :class="category.active ? 'borderme' : 'borderout'"
                class="d-flex align-center rounded-lg mx-2"
                dark
                height="180"
                @click="toggle(category)"
                flat
              >
                <v-row>
                  <v-col cols="12" sm="12">
                    <v-list>
                        <v-list-item three-line class="text-center">
                      <v-list-item-content>
                        <div align="center" justify="center">
                          <v-img
                            :src="category.img"
                            max-height="80"
                            max-width="80"
                            contain
                          ></v-img>
                        </div>
                        <v-list-item-subtitle
                          :class="category.active ? 'text-green' : 'text-black'"
                          class="caption mt-4"
                          >{{ category.title }}</v-list-item-subtitle
                        >
                      </v-list-item-content>
                    </v-list-item>
                    </v-list>
                  </v-col>
                </v-row>
              </v-card>
            </v-item>
          </v-col>
        </v-row>
      </v-container>
    </v-item-group>
  </template>
  
  <script>
  export default {
    data: () => ({
      categories: [
        { img: "01.png", title: "Meat & Fish", active:false },
        { img: "02.png", title: "Vegetables", active:false },
        { img: "3.png", title: "Medicine", active:false },
        { img: "4.png", title: "Baby", active:false },
        { img: "5.png", title: "Office", active:false },
        { img: "6.png", title: "Beauty", active:false },
      ],
    }),
    methods: {
        toggle(category) {
            this.categories.forEach((item) => {
          item.active = false;
      });
  // Tìm đối tượng danh mục dựa trên đối số được cung cấp
  const index = this.categories.findIndex((item) => item === category);

  // Nếu tìm thấy danh mục hợp lệ, hãy chuyển đổi trạng thái hoạt động của nó
  if (index > -1) {
    this.categories[index].active = !this.categories[index].active;
  }
}
    },
  };
  </script>
  
  <style>
  </style>