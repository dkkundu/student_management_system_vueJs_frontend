<template >
<div>
  <h1> Student Data table </h1><br>
</div>


<form class="col my-auto p-3 " method="POST" accept-charset="UTF-8" @submit.prevent="createStudent">
      
      <div class="mb-3 form-group row">
          <div class="form-control d-flex col margin-and_padding"> 
              <input type="test" class="form-control col-4" id="name" placeholder="Name"
              v-model="studentspost.name">
          </div>
          <div class="form-control d-flex col margin-and_padding">
              <input type="number" class="form-control" id="age" placeholder="Age"
              v-model="studentspost.age">
          </div>
          <div class="form-control d-flex col">
              <input type="test" class="form-control margin-and_padding" id="language" placeholder="Languages"
              v-model="studentspost.language.name">
          </div>
         <button type="submit" class="btn btn-primary col margin-and">Submit</button>

      </div>
</form>

<table class="table table-hover">
    <thead>
      <tr>
        <th scope="col">#</th>
        <th scope="col">Name</th>
        <th scope="col">Age</th>
        <th scope="col">Languages</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(student, counter) in students" :key="student.id" >
        <td scope="row">{{counter+1}}</td>
        <td>{{student.name}}</td>
        <td>{{student.age}}</td>
        <td>
          <template v-for="language in student.programming_languages" :key="language.id"> 
            {{ language.name}},
          </template>
        </td>
      </tr>
    
    </tbody>
</table>
</template>

<script>

export default {
  name: 'DataTable',
  data(){
    return {
      studentspost:{
        'name': '',
        'age': '',
        'language': '',

      },
      
      students:[]
    }
  },
  async created(){
    var response = await fetch('http://127.0.0.1:8000/api/student/create/');
    this.students = await response.json();
  },

  methods:{

    async createStudent(){
        var response = await fetch('http://127.0.0.1:8000/api/student/create/',{
          method: 'post',
          headers: {
            'Accept': 'application/json, text/plain, */*',
            'Content-Type': 'application/json'

          },
          body: JSON.stringify(this.studentspost)
        });
        this.studentspost.push(await response.json());

    }

  },

  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.margin-and_padding {
  margin-left: 2%;
  margin-right: 2%;
}
.margin-and {
  margin-left: 2%;
  margin-right: 2%;

}


</style>
