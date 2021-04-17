<script>
    import { items } from "../stores";
    $: itemCount = $items.length;
    $: completedItemCount = $items.filter((item) => item.complete).length;
  </script>
  
  <style>
    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 20px;
      color: #161313;
      font-weight: bold;
      font-size: 1.5em;
      background: rgba(207, 91, 91, 0.1);
    }
  </style>
  
  <div class="header">
    <div>To-Do List✨</div>
    <span> {completedItemCount}/{itemCount} </span>
  </div>