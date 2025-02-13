<script setup>
import { reactive, ref } from 'vue';

 const data=reactive({
  sender:'',
  billTo:'',
  shipTo:'',
  invoiceNumber:'',
  date:'',
  dueDate:'',
  additionalNote:'',
  items:[
    {
      discription:'',
      quantity:'',
      rate:'',
      amount:'',
    }],

  notes:'',
  terms:'',
  subtotal:'',
  tax:'',
  total:''
})

function addMoreItems(){
  data.items.push({
      discription:'',
      quantity:'',
      rate:'',
      amount:'',
    })
}

function getSubTotal(){
  let subtotal=0;
  data.items.forEach(item=>{
    subtotal+=item.amount
  })
  data.subtotal=subtotal
  return subtotal
}

function getTotal(){
  const tax=data.subtotal*data.tax / 100
  data.total=data.subtotal +tax
  return data.total 
}

</script>
 
<template>
 <div class="container mt-4">
        <div class="row">
            <div class="col-md-12 d-flex justify-content-between">
                <div>
                    <img src="./images/invoice-removebg-preview.png" style="width: 100px;" alt="">
                </div>
                <div class="mt-3">
                    <h2>Invoice Generator</h2>
                </div>
                <div>
                    <label class="form-label">Date</label>
                    <input v-model="data.date" type="date" class="form-control">   
                </div>
            </div>
        </div>
        
        <div class="row mt-5">
            <div class="col-md-6">
                <label class="form-label">Sender</label>
                <input v-model="data.sender" type="text" class="form-control" placeholder="Sender Name">
            </div>
            <div class="col-md-3">
                <label class="form-label">Invoice Number</label>
                <input v-model="data.invoiceNumber" type="text" class="form-control" placeholder="#">
            </div>
            <div class="col-md-3">
                <label class="form-label">Due Date</label>
                <input v-model="data.dueDate" type="date" class="form-control">
            </div>
        </div>
        
        <div class="row mt-3">
            <div class="col-md-4">
                <label class="form-label">Bill To</label>
                <input v-model="data.billTo" type="text" class="form-control" placeholder="Client Name">
            </div>
            <div class="col-md-4">
                <label class="form-label">Ship To</label>
                <input v-model="data.shipTo" type="text" class="form-control" placeholder="Shipping Address">
            </div>
            <div class="col-md-4">
                <label class="form-label">Additional Note</label>
                <input v-model="data.additionalNote" type="text" class="form-control" placeholder="Additional Note">
            </div>
        </div>

        <table class="table table-bordered mt-4">
            <thead class="table-dark">
                <tr>
                    <th>Description</th>
                    <th>Quantity</th>
                    <th>Rate</th>
                    <th>Amount</th>
                </tr>
            </thead>
            <tbody>
                <tr  v-for="(item,index) in data.items" :key="index">
                    <td><input v-model="item.discription" type="text" class="form-control"></td>
                    <td><input v-model="item.quantity" type="number" class="form-control"></td>
                    <td><input v-model="item.rate" type="number" class="form-control"></td>
                    <td>
                      ${{ item.amount=item.quantity*item.rate }}
                    </td>
                </tr>
            </tbody>
        </table>

        <button @click="addMoreItems()" class="btn btn-success">Add More</button>
        <p class="mb-5">
          {{ data }}
        </p>

        <div class="row mt-4">
            <div class="col-md-6">
                <label class="form-label">Notes</label>
                <textarea v-model="data.notes" class="form-control" rows="4"></textarea>
            </div>
            <div class="col-md-6 text-end">
                <p >
                  <label>Subtotal:</label>
                  <input :value="getSubTotal()" type="text" name="Subtotal" id="" placeholder="subTotal">
                </p>
                <p >
                  <label>Tax:</label>
                  <input v-model="data.tax" type="text" name="" id="" placeholder="$0.00">
                </p>
                <p >
                  <label>Total:</label>
                  <input :value="getTotal()" type="text" name="Total" id="" placeholder="$0.00">
                </p>
                <p >
                  <label>Balance Due:</label>
                  <input type="text" name="balanceDue" id="" placeholder="$0.00">
                </p>
            </div>
        </div>

        <div class="row mt-3">
            <div class="col-md-6">
                <label for="" class="form-label">Terms</label>
                <textarea v-model="data.terms" name="terms" id="" class="form-control" rows="2"></textarea>
            </div>
            <div class="col-md-6"></div>
        </div>
    </div>
</template>
 
<style scoped>
 
</style>