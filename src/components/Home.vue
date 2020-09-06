<template>
  <div>
    <div id="page-content-wrapper">
        <div id="status-bar" class="container-fluid">
            <div class="row">
                <div class="col-3 col-md-5 col-lg-5">
                    <div class="time-holder">
                        <button class="btn-menu-toggle">
                            <div class="toggle-icon">
                                <div class="icon-shape"></div>
                            </div>
                        </button>
                        <div class="time"><i class="zid zid-clock"></i>الساعة ٨:٣٨ صباحا بتوقيت الرياض</div>
                    </div>
                </div>
                <div class="col-9 col-md-7 col-lg-7">
                    <div class="search-holder">
                        <form><input type="text" placeholder="إبحث هنا..."><button type="submit"><i class="zid zid-find"></i></button></form>
                        <a class="btn-logout" href="#"><span class="text">تسجيل خروج</span><i class="zid zid-exit"></i></a>
                    </div>
                </div>
            </div>
        </div>
        <div class="container-fluid page-head">
            <div class="row">
                <div class="col-md-12">
                    <div class="page-title">طرق الدفع</div>
                    <ol class="breadcrumb breadcrumb-sm">
                        <li class="breadcrumb-item"><a href="settings.html">الإعدادات</a></li>
                        <li class="breadcrumb-item active">طرق الدفع</li>
                    </ol>
                </div>
            </div>
        </div>
        <div class="container-fluid other-content">
            <div class="row">
                <div class="col-12">
                    <div class="alert alert-primary">عند تفعيلك لبوابات الدفع الموضحة ادناه، ستتمكن من ربط متجرك الإلكتروني بإحدى تلك البوابات المختلفة. كل بوابة من البوابات لديها إشتراطات معينة لتفعيل حسابك لديهم. خيارات الدفع تتيح لك استقبال المدفوعات الإلكترونية عبر البطاقات الإئتمانية وبعضهم يدعم خيار: مدى، للدفع الإلكتروني سنقوم بربطك الكترونيًا معهم ولكنك بحاجة أيضًا الى تفعيل اشتراكك لديهم وتعبئة النماذج اللازمة.</div>
                </div>
               
                    <PaymentGateways />
                     <BankTransfer />
            </div>
            <div class="row">
                <div class="col-12">
                    <div class="learn-more-btn-holder">
                        <a href="#" class="btn btn-outline-primary btn-sm">لمعرفة المزيد عن الدفع<i class="fas fa-question"></i></a>
                    </div>
                </div>
            </div>
        </div>
        <div id="footer" class="container-fluid">
            <div class="row">
                <div class="col">
                    <div class="copyright">Copyright <b>Zid App</b> © 2016-2020</div>
                </div>
            </div>
        </div>
        <div class="modal modal-side-text-align fade" id="bankModal" tabindex="-1" role="dialog" aria-hidden="true">
            <div class="modal-dialog modal-md" role="document">
                <div class="modal-content">
                    <div class="modal-header">
                        <div class="modal-title-sm">أضف حساب بنكي</div>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                        </button>
                    </div>
                    <div class="modal-body">
                        <form>
                            <div class="form-row">
                                <div class="col-md-6">
                                    <div class="form-group">
                                        <label for="">اسم البنك</label>
                                        <div class="select-chosen-container select-chosen-container-sm">
                                            <select data-placeholder="Choose a Bank..." class="chosen-select">
                                                <option>البنك الأهلي التجاري</option>
                                                <option>ساب</option>
                                                <option>البنك السعودي الفرنسي</option>
                                                <option>البنك الأول</option>
                                                <option>البنك السعودي للاستثمار</option>
                                                <option>البنك العربي الوطني</option>
                                            </select>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <div class="form-group">
                                        <label for="input1">رقم الحساب</label>
                                        <input type="text" class="form-control form-control-sm" id="input1" placeholder="123456789XXXXXX">
                                    </div>
                                </div>
                            </div>
                            <div class="form-row">
                                <div class="col-md-6">
                                    <div class="form-group">
                                        <label for="input2">الأيبان</label>
                                        <input type="text" class="form-control form-control-sm" id="input2" placeholder="SA03 8000 0000 6080 XXXX XXXX">
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <div class="form-group">
                                        <label for="input3">اسم المستفيد</label>
                                        <input type="text" class="form-control form-control-sm" id="input3" placeholder="Name of the account owner">
                                    </div>
                                </div>
                            </div>
                        </form>
                    </div>
                    <div class="modal-footer">
                        <button type="button" class="btn btn-accept btn-sm">حفظ</button>
                        <button type="button" class="btn btn-grey btn-sm" data-dismiss="modal">إغلاق</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
  
  </div>
</template>

<script>
import PaymentGateways from '../components/PaymentGateways.vue'
import BankTransfer from '../components/BankTransfer.vue'
BankTransfer
export default {
  name: 'Home',
  components: {
    PaymentGateways,
    BankTransfer
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
