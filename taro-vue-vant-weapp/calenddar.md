```javascript
// html
<van-calendar
  :show="showCalendar"
  :poppable="true"
  :round="false"
  :show-mark="false"
  :allow-same-day="true"
  :show-title="true"
  :close-on-click-overlay="true"
  :formatter="formatter"
  position="top"
  type="range"
  color="#22C09F"
  @confirm="onConfirm"
>
  <slot-view name="title">
    <SelectBar
    class="slot-title"
      :showCalendar.sync="showCalendar"
    />
  </slot-view>
  <slot-view name="footer">
    <view class="calendar-footer">
      <view class="btn cancel">清空日期</view>
      <view class="btn confirm">确定</view>
    </view>
  </slot-view>
</van-calendar>
```

```javascript
// js
export default {
  name: '',
  data() {
    return {

    }
  },
  methods: {
    formatter(day) {
      console.log(day)
      day.bottomInfo = '';
      return day;
    },
  }
}
```
